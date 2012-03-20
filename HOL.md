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

<pre><code class="C#"><span style="color:#0000FF">public</span> <span style="color:#0000FF">class</span> GuestBookEntry: Microsoft.WindowsAzure.StorageClient.TableServiceEntity
{
    <span style="color:#0000FF">private</span> <span style="color:#0000FF">string</span> test = <span style="color:#8B0000">&quot;sample text&quot;</span>;
}
</code></pre>

<p>(Code Snippet - <em>Introduction to Windows Azure - Ex1 GuestBookDataSource Fields</em> - CS)</p>
<div class="boxcontent"><div class="boxheader"><p>C#</p></div>
public class GuestBookDataSource{
<div class="CodeHighlighter">
<pre>
<code class="csharp">   private static CloudStorageAccount storageAccount;
   private GuestBookDataContext context;
</code>
</pre>
</div>
}
</div>

<p>(Code Snippet - <em>Introduction to Windows Azure - Ex1 GuestBookDataSource Fields</em> - CS)</p>
<div class="boxcontent"><div class="boxheader"><p>C#</p></div>
public class GuestBookDataSource{
<strong>   private static CloudStorageAccount storageAccount;
   private GuestBookDataContext context;
</strong>
}
<em>
italics adfadf
dafadvadf adf daf a
</em>
</div>

<a name="Exercise1" />
## Exercise 1: Building Your First Windows Azure Application ##

In this exercise, you create a guest book application and execute it in the local development fabric.
