<a name="Title" />
# Introduction to Windows Azure #

---
<a name="Overview" />
## Overview ##

<a name="Exercise1" />
## Exercise 1: Building Your First Windows Azure Application ##

In this exercise, you create a guest book application and execute it in the local development fabric.

<div style="color:red">
test inline style
</div>

<div class="boxcontent"><div class="boxheader"><p>C#</p></div>public class GuestBookDataSource
{
  ...
<strong>   static GuestBookDataSource()
   {
     storageAccount = CloudStorageAccount.FromConfigurationSetting("DataConnectionString");

</strong>
<em>
     CloudTableClient.CreateTablesFromModel(
     typeof(GuestBookDataContext),
     storageAccount.TableEndpoint.AbsoluteUri,
     storageAccount.Credentials);
</em>
  }
}
</div>