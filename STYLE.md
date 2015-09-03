Style Guide
===========
Contributors are expected to follow the conventions outlined in this guide to promote consistency of the codebase. In general, use the [Google style guide][1] with a few exceptions:

 [1]: https://google-styleguide.googlecode.com/svn/trunk/cppguide.html

Always use curley braces
------------------------
Curley braces always go in their own line, even when there is only a single
statement followed by a conditional.
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
80 characters is the maximum column width. Any larger, and you must indent the
following line with a tab.
```cpp
void foo(int someRidiculouslyLargeParameterName,
	int anotherRidiculouslyLargeParameterName)
{
	DoSomething();
}
```

