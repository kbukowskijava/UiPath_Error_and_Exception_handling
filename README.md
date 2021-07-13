# UiPath_Error_and_Exception_handling
Below you can find the most common exceptions that you can encounter in projects developed with UiPath. As a general note, all exceptions are types derived from System.Exception, so using this generic type in a Try Catch, for example, will catch all types of errors.

NullReferenceException - This error usually occurs when using a variable with no set value (not initialized).
IndexOutOfRangeException - Occurs when the index of an object is out of the limits of the collection. 
ArgumentException - Is thrown when a method is invoked and at least one of the passed arguments does not meet the parameter specification of the called method.
SelectorNotFoundException - Is thrown when the robot is unable to find the designated selector for an activity in the target app within the TimeOut period.
ImageOperationException - Occurs when an image is not found within the TimeOut period.
TextNotFoundException - Occurs when the indicated text is not found within the TimeOut period.
ApplicationException - describes an error rooted in a technical issue, such as an application that is not responding.
Business Rule Exceptions are separate from all the System Exceptions listed above. These describe errors rooted in the fact that certain data which the automation project depends on is incomplete, missing, outside of set boundaries (like trying to extract more from the ATM than the daily limit) or does not pass other data validation criteria (like an invoice amount containing letters).

The Business Rule Exceptions will not be thrown by using the generic System.Exception in a Try Catch activity. The mechanism of handling this exception has to be separately defined by the developer (based on the rules set by the process owner), or it can be reduced to stopping the execution of the process, by using a simple Throw activity, for example.
