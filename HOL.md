<a name="Title" />
# Introduction to Windows Azure #

---
<a name="Overview" />
## Overview ##

<a name="Exercise1" />
## Exercise 1: Building Your First Windows Azure Application ##

In this exercise, you create a guest book application and execute it in the local development fabric.

<!-- mark:2 -->
````C#
public class GuestBookEntry
	: Microsoft.WindowsAzure.StorageClient.TableServiceEntity
{
}
````


(Code Snippet – _Introduction to Windows Azure - Ex1 GuestBookDataSource Static Constructor_ – CS)

<!-- mark:4-12 -->
````C#
public class GuestBookDataSource
{
  ...
   static GuestBookDataSource()
   {
	 storageAccount = CloudStorageAccount.FromConfigurationSetting("DataConnectionString");

	 CloudTableClient.CreateTablesFromModel(
	 typeof(GuestBookDataContext),
	 storageAccount.TableEndpoint.AbsoluteUri,
	 storageAccount.Credentials);
  }
}
````

<!-- mark:4-8 -->
```` C#
public class GuestBookDataSource
{
  ...
  public GuestBookDataSource()
  {
    this.context = new GuestBookDataContext(storageAccount.TableEndpoint.AbsoluteUri, storageAccount.Credentials);
    this.context.RetryPolicy = RetryPolicies.Retry(3, TimeSpan.FromSeconds(1));
  }
}
````
