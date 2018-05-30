pyWinErrors
===========


A collection of 2838 Windows Error codes as returned by kernel32.GetLastError.

I have included some extras in this package

`format_error` - a function that when passed an error code retrieves a
human readable string from Windows and converts the decimal error code
into the typical 0 padded hex. It puts these 2 together and returns the
string.

`GetLastError` - a function that retrieves the last error that has occurred.

`WindowsAPIError` - an exception subclass that when passed a decimal
error code creates an exception containing a formatted human readable
output of the error. The original error code can be retrieved from the
exception instance by referencing index 1 as if the instance was a list.
You can also pass an error code as a string if you wanted. in this case
the error code that is stored in the exception is None
