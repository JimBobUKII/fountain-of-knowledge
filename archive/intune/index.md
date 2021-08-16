# Intune Introduction

## A Foundation of Active Directory Domains

So I would start out by doing a drawing to help everybody understand some of the fundamentals of where the industry was, where it is, and kind of where things are flowing right now, especially from the standpoint of Microsoft. So I want to I want to kind of take you back in time a little bit and help you understand it, really help you understand where things are moving right now. If you can also sort of look at where things were at one time.

So if you went back far enough, course, I'm not going to go back too far. You had the 1960s, you had mainframes and you had is moved into the 1970s. You also had mainframes, these massive computers that were like room size or at least refrigerator size in most cases.

And then as we moved into the 1980s and standardization occurred, computers, the pricing of computers went down and companies could actually afford to get what is called a personal computer. And of course, with the invention of that concept, you had what was called peer to peer networking.

Few personal computers, let's say that in your in your organization, your company has a thousand computers.



Because it's going to draw a bunch of things and it kind of gets overwhelming when there's a bunch of things on the screen. OK, so we start out with a bunch of computers that say we have a thousand computers now from a from an I.T. person standpoint is we moved in the 1980s and computer in companies wanted to share resources with each other.

There was different companies that played a role in this. Microsoft played a role in it with DOFFS and the land manager. Then a company called Novell played a huge role in it. Course, it was also Unix. Then we moved into the 1990s and this became more and more popular as time went on and as companies grew and started needing to be able to manage more and more computers, they needed a system for doing that. And at the time, all we had was what was known as a peer to peer network, which meant every computer is sort of on its own. And that meant that you had to sit down and configure each computer individually. Imagine doing that with a thousand computers.

One solution to that was to create scripts, log on scripts that would would automate the process of set things computers up. But it was still a lot of work. And if you had to change one thing on one machine, you had to change it on the others and you had to every computer had to have usernames and passwords that were separate from the others and it just got crazy.

So what Microsoft did and again, we were kind of focused on Microsoft here, is they created the concept of of what is called a domain and in their concept was based on some concepts that Novell had implemented and Unix had implemented. And by the time we reached the Nate, the late 1990s, by the time we reached the late 1990s, Microsoft had released in 84 and had domains and the goal of a domain with centralization.

Microsoft created a new directory service and a new concept for domains.  In fact, the symbol of what is called a Microsoft domain is the symbol of a triangle. So they created this triangle, this domain and the domain would act sort of as the security boundary for your company.

So your computers would go inside the security boundary. You had a thousand computers here, part of the security boundary course, something that you did need to to deal with all this if you needed servers that could help you manage these computers. So with that, Microsoft had what was called a domain controller. A domain controller is a server that has a special database.

This little cylinder looking thing that I'm drawing is going to be a symbol of a database right here. And that database is called Active Directory. Aidi Active Directory is the directory services structure that manages are Microsoft domains. Now, that directory service is where your user accounts, passwords, groups, all of that stuff is is going to live. And with the creation of domain controllers also came these things called a group policy objects. GPOs allow us to deploy restrictions and settings out to all these machines. So I have the ability to implement this thing called a GPO and the geos can deploy it can apply to all of these computers and they get configured based on the GPO. And of course, generally speaking, when it comes to a domain controller ADC, you want to have more than one of those.

So what do you want to have more than one domain controller to manage everything? Well, it's kind of the same reason that we want. If you go to a grocery store and you get a cart load of groceries and you're you're checking out and in, you're taking your cart load of the groceries to the front of the store to check out, the last thing you want to see is for there to be one cashier open, one cash register open to check you out. What do you want to see when you get up there? You want to see a lot of open aisles of cash registers with people work in those cash registers where I can check out and buy my stuff and leave. What I don't want to do is get to the front and there are only to be one cash register open and there's a line of people waiting to get out.

All of these computers right here, these 1000 computers that I have need to talk to these domain controllers if I've only got one. Then you've got you've got one machine that's basically having to manage everybody. So you want to more than one. There's basically two main reasons why we have more than one of anything.

Redundancy also known as fault tolerance and load balancing. So if one domain controller fails, we've got another one run in.

The other reason is for performance. We don't want all of these clients, all of these machines having to just go to. One dimensional, we prefer them to go to multiple now.

The other great thing about domain controllers, when you when you think about domain chores is domain controllers replicate. So anything I do to one domain controller, like let's say that this little smiley face guy here that 

This guy is a user account. So what's going to end up happening is your user account. You create this user account on this domain controller. Guess what it's going to replicate to this other domain controller over here. And it synchronizes that way through what is known as active directory replication. 

So if you were to come to me and you were to to say, why am I needing. To have a domain, why not just stick with the old style, which was peer to peer networking? This is what I would tell you. I would say centralization. That's why I can tell you why act directory is so important in one word, centralization.

A lot of people would say security, security is important, but centralization is why this is so such a key thing we use in our environments. I can manage everything using these domain controllers. I want my company can actually have multiple domains. There's these things called trees and forest. I'm not going to get into that right now, but I can manage my infrastructure using active directory. 

Now, there are some other key fundamentals to understand about Active Directory. First off, the naming system that Active Directory uses that domains used for managing everything is based upon DNS domain name system. Your domain name will have to be named based upon a DNS style name. So, for example, if I work for a company called Exam Lab Practice and my web presence is exam lab practice dot com, then my domain name may also be called exam lab practice dot com. That might be the name of my DNS name. OK, and all my computers will be based on that DNS name. So if I had a computer called Client One, his his DNS name had fully qualified domain name as it's called, might be called client one dot exam, lab practice, dot com inside this domain. But on top of that you have to have a server that's going to manage all that. So we have to have something called a DNS server domain name system server.

What's that going to do? Well, we need domain name servers for the same reason you have an address book with your phone. You don't you don't really like having to memorize lots of phone numbers. So you have an address book. You're able to type somebody's name and their phone number in. And then later you can access their name and get access to the phone number and make the call. Well, DNS does that, except it does it for IP addresses. All these devices have IP addresses and they're going to be registered into your DNS database.

Now bring and saying that database, that means that there's also got to be a database on that DNS server. The DNS database is often called a zone database. It's often called a namespace database. And from there, I'm just gonna kind of color code.

This will say that exam lab practice, dot com being the company's name in this database you see here is going to manage that, some highlighting it in red, just like it is basically bordered it in red as well. So we got to have DNS. Now, what's going to happen is these computers are all gonna boot up, including if I heads a server. These computers are all gonna boot up and they're going to register with DNS, including this file server guy here that I'm making him. I call him file server. So they're gonna boot up and they're all going to register their names in DNS. The domain controllers are gonna register, the file servers are going to register. Everything's going to register inside DNS. This is what this is a topic known as Dynamic DNS. And this is going to allow computers to all register.

Now, what happens is every one of these machines, your client computers, your servers, they all have to locate DNS by their IP settings and they're gonna ask DNS who these guys right here are so that they can all authenticate. So these clients, when they boot up, they're going to say, hey, DNS. Do you happen to know who my domain controllers are for my environment? And DNS is going to reply back with this this information known as service records as arvi information. And it's going to point the client to these domain controllers.

The other great thing about Active Directory Active Directory supports the ability to point people to the nearest domain controller so that they can log on and get authenticated. The authentication system that Active Directory uses is based on a protocol called Kerberos. When you hear that name protocol, I want you to think language. It's basically like a language. They speak in an active directory. Security and querying language is built off of two two protocols, really. One of them is called LDAP. Lightweight Directory Access Protocol, which is basically a query language. And Kerberos, which is going to be your security authentication language that it uses.

So as we moved into the year 2000, Active Directory was released and this was the big thing everybody's doing. And of course, you know, the big thing, too, is we also have to have an Internet connection. So this little this little cloud thing that I that I just made here, this is gonna be my my Internet connection. And so we've got an Internet connection coming into our company here. And we're also gonna have to protect our Internet. So we're gonna have a firewall. So this little guy right here be my firewall and my firewall is connected to. My internal network, as well as my outside world Internet connection, of course. You know, it's routing is involved there. And and all that stuff as well.

So the Internet is the big thing. Everybody's want to be on the Internet and be secure and build access resources. And so Microsoft is making technologies that are available to do this, though. LDAP and Kerberos are both internal based technologies that are not really stuff, something that you exposed to the Internet, which is why you got to have protection and and all of that.

## A Foundation of RAS, DMZ, and Virtualization
## A Foundation of the Microsoft Cloud Services
## Creating a free Microsoft 365 Azure AD Account
## Introduction to Intune
## Using the Endpoint Manager Portal to manage Intune

