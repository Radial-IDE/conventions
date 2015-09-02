Style Guide
===========
Contributors are expected to following the following guidelines  to keep the
codebase consistent. In general, use the [Google style guide][1] with a few
differences:

 [1]: https://google-styleguide.googlecode.com/svn/trunk/cppguide.html

Always use curley braces
------------------------
Curley braces always go in their own line, even when there is only a single
statment followed by a conditional.
```
if (condition)
{
	DoSomething();
}
```

Use tabs rather than spaces
----------------------------
Note, that access modifiers and case keywords go in the root indent level.
```
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
```
void foo(int someRidiculouslyLargeParameterName,
	int anotherRidiculouslyLargeParameterName)
{
	DoSomething();
}
```

