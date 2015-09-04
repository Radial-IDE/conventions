Style Guide
===========
Contributors are expected to follow the conventions outlined in this guide to promote consistency of the codebase. In general, use the [Google style guide][1] with the following exceptions:

 [1]: https://google-styleguide.googlecode.com/svn/trunk/cppguide.html

File types
----------
Use `.hpp` for C++ header files and `.cpp` for C++ files.

Always use curley braces
------------------------
Curley braces always go in their own line, even when there is only a single statement followed by a conditional.
```cpp
if (condition)
{
	DoSomething();
}
```

Use tabs rather than spaces
----------------------------
Note, that access modifiers and case keywords go in the root indent level.
```cpp
class MyClass
{
public:
	MyClass();

private:
	bool SomeInternalFunction();
};

bool MyClass::SomeInternalFunction()
{
	switch (enumerable)
	{
	case 1:
		return true;
	default:
		return false;
	}
}
```

Break up long lines using a tab indent
--------------------------------------
80 characters is the maximum column width. Any larger, and you must indent the following line with a tab.
```cpp
void foo(int someRidiculouslyLargeParameterName,
	int anotherRidiculouslyLargeParameterName)
{
	DoSomething();
}
```

Constructor initializer lists
-----------------------------
Constructor initializer lists can be all on one line or with subsequent lines indented with a tab following a comma and a space.

There are two acceptable formats for initializer lists:

```cpp
// When it all fits on one line:
MyClass::MyClass(int var) : some_var_(var), some_other_var_(var + 1) {}
```

or

```cpp
// When it requires multiple lines, indent 1 tab, putting the colon on the first
// initializer line:
MyClass::MyClass(int var)
	: some_var_(var)           // tab indent
	, some_other_var_(var + 1) // lined up
{
	...
	DoSomething();
	...
}
```
