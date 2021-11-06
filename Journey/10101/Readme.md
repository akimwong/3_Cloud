<p align="left">
  <img src="Budgets.png" width="50" height="50">
  <img src="LongTermSecCred.png" width="50" height="50"></p>

# AWS Platform SetUp

Steps:<br/>
<br/>
1º [Create a new AWS ROOT account (in spanish)](https://www.youtube.com/watch?v=8AUWxW14lhk&t=4s) to start the practice.   As new user, at the beginning you will use the "console interface".  You `MUST` define the credit limit alarms described in the video using the tool `Budgets`<br/>
2º Using the "console interface" (again) create your personal account (to `avoid the use in the future the use of the ROOT account`), assign the policy `System Administrator`, [generate your Access Key/Secret Access Key (in spanish)](https://www.youtube.com/watch?v=_zMCdUndHy0&t=239s) and set up in your local computer to communicate with AWS in a programatic way<br/>
3ª CLOSE the ROOT account and storage the access information in a safe place.  Now, you can interact with AWS<br/>
4º [Access to boto3 official documentation](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html) that contains all the syntaxis, commands, tools and options that can be use to interact with AWS <br/>

<p align="left">
  <img src="SDK.png" width="50" height="50"></p>
  
## WHY TO USE CLI/SDK INSTEAD CONSOLE?

Through the console, you can manage your AWS resources visually and in a way that is easy to digest. `THIS IS GREAT FOR GETTING STARTED AND BUILDING YOUR KNOWLEDGE` of the services. It's also useful for building out test environments or viewing AWS bills, viewing monitoring and working with other non technical resources. The AWS Management Console is most likely the first place you will go when you are learning about AWS 


However, once you are up and running in a production type environment, you don't want to rely on the point and click style that the console gives you to create and manage your AWS resources. For example, in order to create an Amazon EC2 Instance, you need to click through various screens, setting all the configurations you want, and then you launch your instance. If later, you wanted to launch another EC2 Instance, you would need to go back into the console and click through those screens again to get it up and running. `By having humans do this sort of manual provisioning, you're opening yourself up to potential errors. It's pretty easy to forget to check a checkbox or misspell something when you are doing everything manually` 


The answer to this problem is to use tools that allow you to script or program the API calls. One tool you can use is the AWS Command Line Interface or CLI. The CLI allows you to make API calls using the terminal on your machine. This is different than the visual navigation style of the Management Console. `Writing commands using the CLI makes actions scriptable and repeatable.` So, you can write and run your commands to launch an EC2 Instance. And if you want to launch another, you can just run the pre-written command again. `This makes it less susceptible to human error.` And you can have these scripts run automatically, like on a schedule or triggered by another process 


Automation is very important to having a successful and predictable cloud deployment over time. Another way to interact with AWS is through the AWS Software Development Kits or SDKs. The SDKs allow you to interact with AWS resources through various programming languages. This makes it easy for developers to create programs that use AWS without using the low level APIs, as well as avoiding that manual resource creation that we just talked about.
