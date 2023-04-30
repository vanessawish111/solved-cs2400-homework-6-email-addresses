Download Link: https://assignmentchef.com/product/solved-cs2400-homework-6-email-addresses
<br>



Search engine companies, like Google, often search internet websites for the purpose of data collections. Programs, called web scrapers, collect information for the purpose of indexing the sites and collecting other information such as email addresses, phone numbers, etc. You’ve been asked to access a website and only extract email addresses from it. The site file often has the extension “.html”. See below for an example site that you can use.

Email addresses are tagged within the site as follows (note that other formats may be included):




&lt;a href=”mailto:<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="aac8c5c8eac5c2c3c584cfcedf">[email protected]</a>”&gt; Send email &lt;/a&gt;

&lt;a href=”mailto:<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="abc9c4c985d8c6c2dfc3ebcac8ce85c4c3c2c485cecfde">[email protected]</a>”&gt; Send email &lt;/a&gt;

&lt;a href=”mailto:<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="41232e2301232e236c222035326f2e29282e6f242534">[email protected]</a>”&gt; Send email &lt;/a&gt;




Where “<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="294b464b6946414046074c4d5c">[email protected]</a>” is the email address, “bob” is the user name, and “ohio.edu” is the domain name.

Write a program that processes a website file and extracts all the email addresses from the site and stores the emails in <em>parallel</em> arrays or vectors (emails, users, domains). If you’re using arrays, you may assume that the number of emails will not exceed <strong>1000</strong>. You only need to extract email addresses that conform to the tag formats specified above.

Output the following the number of lines process and the number of unique emails extracted to the screen:




51 lines processed

20 emails found




Write a function that outputs the data to a file as follows:




Email                         user           domain

————————————————————–

b<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="4a25280a25222325642f2e3f">[email protected]</a>                  bob            ohio.edu

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="6f0d000d411c02061b072f0e0c0a410c1c4100070600410a0b1a">[email protected]</a>     bob.smith      ace.cs.ohio.edu <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="2043531214101060474d41494c0e434f4d">[email protected]</a>         cs2400    gmail.com

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="93f1fcf1d3f1fcf1bef0f2e7e0bdfcfbfafcbdf6f7e6">[email protected]</a>         bob            bob-cats.ohio.edu




Read the input file one line at a time (<strong>hint: use getline</strong>) and process it. Note that a line may have more than one email address. Process lines until the end of the input file is reached. For each email address extracted, split it into a <em>user</em> and a <em>domain</em>. Use three arrays to store the email addresses, users, and domains.  <strong>Before storing the email into the arrays, make sure the email is not in the array already</strong>. The array of emails should only contain unique email addresses. Your program should only output unique email addresses to the output file.




The name of the input and output file names must be provided at the command line. For example:

./a.out website.html output.txt

Report errors if the number of arguments is incorrect or the either file is not accessible.




<strong>You may use any function or library discussed in class or in the chapters we covered from your textbook. Do not use any other libraries or functions. </strong>

<strong> </strong>

<strong>Hints: </strong>

<ul>

 <li>splitEmailAddress: A function that splits an email address and returns the two parts of it as reference parameters.</li>

 <li>isFound: A search function for an array of strings.</li>

 <li>getLineEmails: A function that takes a string and extracts all the emails from a single line into the parallel arrays and check for uniqueness. You may want to call splitEmailAddress each time.</li>

</ul>




<strong>How to get a sample data file </strong>

<ul>

 <li>Browse to the website</li>

 <li>https://www.ohio.edu/engineering/about/people/departmentallisting.cfm#ElectricalEngineeringandComputerScience</li>

 <li>Save the source code of the file o In Chrome: Right click on the page background, select save as “html” file. Choose a name for the file. o In Safari: Right click on the page background, select “Save Page as” and make sure the “Page Source” is selected. Choose a name for your file.</li>

 <li>A sample file is provided with the assignment.</li>

</ul>