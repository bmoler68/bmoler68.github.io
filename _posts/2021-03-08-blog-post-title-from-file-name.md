## Blog Post Title From First Header

Due to a plugin called `jekyll-titles-from-headings` which is supported by GitHub Pages by default. The above header (in the markdown file) will be automatically used as the pages title.

If the file does not start with a header, then the post title will be derived from the filename.

This is a sample blog post. You can talk about all sorts of fun things here.

---

### This is a header

#### Some T-SQL Code

```tsql
SELECT This, [Is], A, Code, Block -- Using SSMS style syntax highlighting
    , REVERSE('abc')
FROM dbo.SomeTable s
    CROSS JOIN dbo.OtherTable o;
```

#### Some PowerShell Code

```powershell
Write-Host "This is a powershell Code block";

# There are many other languages you can use, but the style has to be loaded first

ForEach ($thing in $things) {
    Write-Output "It highlights it using the GitHub style"
}
```

#### Some Kotlin Code
```kotlin
fun main(args: Array< String >) 
{val str1: String? = “Hello World”var str2: String? = null 
// prints String is nullif(str1 is String) 
          {// No Explicit type Casting needed.println(“length of String ${str1.length}”)}
else 
          {println(“String is null”)}}
```
