---
tags: Test
---

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
{val str1: String? = "Hello World"var str2: String? = null 
// prints String is nullif(str1 is String) 
          {// No Explicit type Casting needed.println("length of String ${str1.length}")}
else 
          {println("String is null")}}
```

#### Some Bash Code
```bash
#!/bin/bash
name="World"
echo "Hello, $name!"
for i in {1..5}; do
    echo "Iteration $i"
done
```

#### Some Java Code
```java
public class HelloWorld {
    public static void main(String[] args) {
        String message = "Hello, World!";
        System.out.println(message);
        
        int sum = 0;
        for (int i = 1; i <= 10; i++) {
            sum += i;
        }
        System.out.println("Sum: " + sum);
    }
}
```

#### Some JavaScript Code
```javascript
function greet(name) {
    return `Hello, ${name}!`;
}

const users = ['Alice', 'Bob', 'Charlie'];
users.forEach(user => {
    console.log(greet(user));
});

// Arrow function example
const add = (a, b) => a + b;
console.log(add(5, 3));
```

#### Some JSON Code
```json
{
  "name": "John Doe",
  "age": 30,
  "city": "New York",
  "hobbies": ["reading", "coding", "hiking"],
  "address": {
    "street": "123 Main St",
    "zipcode": "10001"
  }
}
```

#### Some Perl Code
```perl
#!/usr/bin/perl
use strict;
use warnings;

my $name = "World";
print "Hello, $name!\n";

my @numbers = (1, 2, 3, 4, 5);
foreach my $num (@numbers) {
    print "$num\n";
}
```

#### Some Python Code
```python
def greet(name):
    return f"Hello, {name}!"

class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def introduce(self):
        return f"I'm {self.name} and I'm {self.age} years old."

person = Person("Alice", 30)
print(person.introduce())
```

#### Some Shell Code
```shell
#!/bin/sh
echo "Hello from shell script"
count=0
while [ $count -lt 5 ]; do
    echo "Count: $count"
    count=$((count + 1))
done
```

#### Some SQL Code
```sql
SELECT 
    u.id,
    u.name,
    COUNT(o.id) AS order_count
FROM users u
LEFT JOIN orders o ON u.id = o.user_id
WHERE u.created_at > '2024-01-01'
GROUP BY u.id, u.name
HAVING COUNT(o.id) > 0
ORDER BY order_count DESC;
```

#### Some XML Code
```xml
<?xml version="1.0" encoding="UTF-8"?>
<bookstore>
    <book id="1">
        <title>Introduction to Programming</title>
        <author>John Smith</author>
        <price>29.99</price>
    </book>
    <book id="2">
        <title>Advanced Algorithms</title>
        <author>Jane Doe</author>
        <price>49.99</price>
    </book>
</bookstore>
```

#### Some YAML Code
```yaml
name: John Doe
age: 30
city: New York
hobbies:
  - reading
  - coding
  - hiking
address:
  street: 123 Main St
  zipcode: 10001
skills:
  programming:
    - Python
    - JavaScript
    - Java
  level: advanced
```
