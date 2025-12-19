---
tags: ["2025", "Development"]
---

## Using Published Google Forms and Sheets as a Data Source

When I started working on the requirements for the Borderlands SHiFT Code application I needed a way to provide data to the app without building a complex backend infrastructure. As my first AI generated Android application, I wanted to keep it reasonably simple.  Unfortunately, Gearbox Software does not appear to have a public API that could be used to obtain this data directly from the SHiFT servers.  So I wanted to find a solution that would allow me to quickly provide new codes to the mobile app anytime I would see them on the Gearbox social accounts.

After doing some research, I read about a surprisingly simple solution of using published Google Forms and Google Sheets as a data source. It turned out to be the perfect low-code approach for my needs, and I thought I'd share how it works in case it helps others in similar situations.

### The Problem I Was Trying to Solve

For the Borderlands SHiFT Codes app, I needed a way to:
- Build a repository of SHiFT codes whether they are active, expired or non-expiring
- Have an interface that could be used to update the repository
- Make the data accessible to the Android app without building a complicated backend
- Keep the solution simple and maintainable

Building a traditional backend with a database and API seemed like overkill for this particular application.  The function of this Android app was to simply provide a way to present new SHiFT codes to the community via an app as a convenience.  These SHiFT codes are public data and would not be high-volume, so a secure and scalable solution was not required.

### The Solution: Google Forms + Sheets Pipeline

Google Forms and Google Sheets work together to create a simple but powerful data pipeline. Here's how I set it up:

#### Step 1: Create and Configure the Form

I started by creating a Google Form with well-structured questions. The key here is to think about how your data will be used later.  Use clear, concise labels that will map cleanly to column headers in the sheet. I made sure to enable required fields and use data validations via regular expressions to maintain the quality of the dataset.

#### Step 2: Link the Form to a Sheet

In the Form editor, I navigated to **Responses → Link to Sheets** and created a new spreadsheet. Every form submission automatically appends a new row to the sheet, creating a live datastore that updates in real-time.

#### Step 3: Publish the Form

Once the form was set up, I clicked the **Send** button and copied the link. I could share the form link with others who might want to contribute SHiFT codes, or I could use it myself to add new entries. The sharing settings let me control who can access it.

#### Step 4: Publish the Sheet

I opened the linked Google Sheet and went to **File → Share → Publish to the web**.  I then selected **CSV** as the format. Google generates a public URL that serves the sheet data as a CSV file, which can be consumed directly by applications.

This published CSV URL became my app's data source. The Android app could simply make an HTTP request to this URL, download the CSV, parse it, and display the data. No backend needed!

### How It Works in Practice

The workflow is simple:

**[User Input via Google Form] → [Google Sheet (live response log)] → [Published CSV → Public Data Source]**

For my Borderlands SHiFT Codes app, this meant:
1. I (or others) could submit SHiFT codes through the Google Form
2. The data automatically appeared in the linked Google Sheet
3. The published CSV URL always served the latest data
4. My Android app fetched and parsed this CSV on startup or when refreshing

### Best Practices I Learned Along the Way

After using this approach, here are some things I'd recommend:

- **Data Hygiene**: Use consistent naming conventions for your column headers (I prefer snake_case or camelCase) to make parsing easier in your app.  I also highly recommend the use of required fields and data validation using regular expressions to maintain the integrity of the data entered in the form.
- **Availability Considerations**: On rare occasion, Google will make an update to Sheets that will force sheets published as a CSV URL to be treated as a HTML URL instead.  In my case, I created a self-published fallback CSV URL on my own server as a form of fault tolerance for the app whenever this occurs.  If your app has uptime requirements, I would recommend having a backup solution in place.
- **Security Considerations**: If you're collecting sensitive data, make sure to limit form access appropriately. For public data like SHiFT codes, this wasn't a concern
- **Schema Documentation**: Document your data structure somewhere as this will help when you're writing the parsing logic in your app
- **Automation Options**: If you need more control, you can use Google Apps Script or the Drive API to automate exports, but for my use case, the simple published CSV was perfect

### Why This Approach Worked for Me

Using Google Forms and Sheets as a data source was ideal for my first Android app because:

1. **No Backend Required**: I could focus entirely on developing the app without getting distracted by server-side concerns
2. **Easy Updates**: Adding new SHiFT codes was as simple as filling out a form
3. **Real-time Data**: The published CSV always reflected the latest data in the sheet
4. **Low Maintenance**: Once set up, it required minimal ongoing maintenance
5. **Free**: Google's tools are free to use, which was perfect for a hobby project

### Conclusion

Publishing Google Forms and Sheets as a public data source transformed what could have been a complex backend project into a simple, manageable solution. For the Borderlands SHiFT Codes app, it provided exactly what I needed: a way to collect, store, and serve data without building unnecessary infrastructure.

This approach might not be suitable for every application.  If you need complex queries, authentication, or high-performance requirements, you'll eventually need a proper backend. But for simple data collection and distribution, especially when you're learning or prototyping, it's a surprisingly powerful solution that lets you focus on what matters most: building your app.

If you're working on your first mobile app and feeling overwhelmed by the prospect of building a backend, consider giving this approach a try. Sometimes the simplest solution is the best one.
