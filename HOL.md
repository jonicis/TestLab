<a name="Title" />
# Introduction to Windows Azure #

---
<a name="Overview" />
## Overview ##

	(Code Snippet - _ExploringWindowsAzureStorage-Ex01-06-MessagesProperty-CS_)
	<!--mark: 5-11-->
	````C#
	public class MessageDataServiceContext
	    : TableServiceContext
	{
	  ...
	  public IQueryable<Message> Messages
	  {
	    get
	    {
	      return this.CreateQuery<Message>("Messages");
	    }
	  }
	}
	````

<a name="Exercise1" />
## Exercise 1: Building Your First Windows Azure Application ##

In this exercise, you create a guest book application and execute it in the local development fabric.
