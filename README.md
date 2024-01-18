EXCEPTION HANDLER MODULE

Module Overview:
This module defines a custom exception handler class, CustomExceptionHandler, which captures and logs exceptions. It provides a mechanism to map specific exception types to custom error codes and messages.

Class: CustomExceptionHandler:

Constructor (__init__):

Parameters: action (str) - A string describing the action during which the exception occurred, exception (Exception) - The exception object.
Initializes the CustomExceptionHandler instance by extracting error information and logging the error.
Method: extract_error_info (staticmethod):

Parameters: exception (Exception) - The exception object.
Returns a tuple containing error code and error message based on the type of the provided exception. If the exception type is not explicitly handled, it defaults to code 499 and the exception's string representation.
Method: log_error:

Parameters: action (str) - A string describing the action during which the exception occurred, exception (Exception) - The exception object.
Logs the error information, including the action, error code, and error message. The error message is printed to the console and appended to an "error_log.txt" file.
Error Code Mapping:

The extract_error_info method defines a mapping of specific exception types to custom error codes and messages.
Example mappings include ZeroDivisionError, ValueError, TypeError, etc.
If an exception type is not explicitly handled, it defaults to the generic code 499 and the exception's string representation.
Usage:

Create an instance of CustomExceptionHandler when handling exceptions in your code, providing details about the action and the exception itself.
Note:

Ensure you have appropriate permissions to write to the "error_log.txt" file and handle file-related exceptions if necessary.
