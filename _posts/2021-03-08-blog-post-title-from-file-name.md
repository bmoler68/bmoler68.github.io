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

#### Some Python Code

```python
def flatten_list(nested_list):
    if not(bool(nested_list)):
        return nestedList
 
    if isinstance(nested_list[0], list):
        return flatten_list(*nested_list[:1]) + flatten_list(nested_list[1:])
 
    return nested_list[:1] + flatten_list(nested_list[1:])
```

#### Some Kotlin Code

```kotlin
class MainActivity : AppCompatActivity() {
    private lateinit var viewModel: MainViewModel
    
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        
        viewModel = ViewModelProvider(this)[MainViewModel::class.java]
        
        viewModel.data.observe(this) { data ->
            // Update UI with data
            updateUI(data)
        }
    }
}
```

#### Some Java Code

```java
public class MainActivity extends AppCompatActivity {
    private MainViewModel viewModel;
    
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        
        viewModel = new ViewModelProvider(this).get(MainViewModel.class);
        
        viewModel.getData().observe(this, data -> {
            // Update UI with data
            updateUI(data);
        });
    }
}
```

#### Some JavaScript Code

```javascript
// Async function example
async function fetchUserData(userId) {
    try {
        const response = await fetch(`/api/users/${userId}`);
        const data = await response.json();
        return data;
    } catch (error) {
        console.error('Error fetching user data:', error);
        throw error;
    }
}
```

#### Some JSON Code

```json
{
    "name": "Android App",
    "version": "1.0.0",
    "dependencies": {
        "kotlin": "1.9.0",
        "androidx.compose": "1.5.0"
    },
    "features": [
        "syntax highlighting",
        "code formatting",
        "language support"
    ]
}
```

#### Some XML Code

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android">
    <application
        android:label="@string/app_name"
        android:icon="@mipmap/ic_launcher">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>
</manifest>
```

#### Some YAML Code

```yaml
app:
  name: Android Development Blog
  version: 1.0.0
  author: Brian Moler
  
dependencies:
  - kotlin: 1.9.0
  - androidx.compose: 1.5.0
  
features:
  - syntax highlighting
  - multiple language support
  - code formatting
```

#### Some Shell Code

```shell
#!/bin/bash
# Build Android project
./gradlew clean build

# Run tests
./gradlew test

# Install debug APK
./gradlew installDebug
```

#### Some CSS Code

```css
.container {
    display: flex;
    flex-direction: column;
    padding: 16px;
    background-color: #ffffff;
}

.title {
    font-size: 24px;
    font-weight: bold;
    color: #333333;
    margin-bottom: 16px;
}
```