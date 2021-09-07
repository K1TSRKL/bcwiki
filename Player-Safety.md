We know, security is boring. But safety is one of the core principles of practicing BDSM, and we'd encourage you to take the same approach in the game. If you can spare 10 minutes to read through this page, you'll know just about everything you need to stay safe in the club.

## Table of Contents

* [Account security](#account-security)
* [Scripts & browser extensions](#scripts--browser-extensions)

---

## Account security

Your Bondage Club account password is encrypted on the game's server, but this doesn't mean you should be lax about protecting your details. Here are a few things you should think about to keep your account protected.

### Keep your account name and password private

Much like every other online account you might possess, the number one rule for protecting your account is:

> ⚠️ **Never give anyone your account name or password**

### Use strong passwords

Even if nobody knows your password, that doesn't matter if it's easy to guess or brute-force.

* Avoid common passwords. [Check your password against this list][1] (you can press `Ctrl+F` to search for your password in the list). If your password is on there, it's strongly recommended that you change it.
* Keep your passwords as long as possible. Length is the easiest way to make passwords difficult to brute-force. Bondage Club currently supports alphanumeric passwords of up to 20 characters in length, and we recommend that you make use of as much of that length as you can.
* If you use the same password across different accounts and services, check your email address(es) against [Have I Been Pwned][2] - this will let you know if your email address and/or corresponding password has been leaked in a data breach, and when it happened. If it has, and you're still using the same password, it's strongly recommended that you change your password for that email address and any other services that use the same password.

### Link an email address

We'd also recommend connecting an email address to your Bondage Club account, which you can do through your account Security Preferences page. This will allow you to reset your password or recover your account in the event that you lose access to it. Your email is stored on the game's server and never sent to game clients (even your own), and is not used for anything other than password resets and account recovery.

> ℹ️ If you lose access to (or forget) your email address, you will be unable to reset your password or recover your account

### Don't visit weird links

As with everywhere else on the internet, don't visit links that people post in chatrooms unless you trust the sender or are confident that the link is safe.

---

## Scripts & browser extensions

If you've been around the multiplayer portion of the game for a little while, you've probably run across console users, scripted rooms, and custom browser extensions for the club. This section will tell you what you need to know about staying safe when using or interacting with custom scripts.

### What are scripts?

> Bondage Club is written in [JavaScript][3] and runs in the browser. Scripts are pieces of JavaScript code that players can run in their browser to modify aspects of the game. Most browsers come with built-in developer tooling where you can run arbitrary JavaScript code.

### Are scripts banned in the club?

> No. You are free to use scripts to enhance your game experience, but you should always make sure that you definitely know what a script does before using it.

### What's the worst that can happen if I run a script?

> A lot. Scripts run inside your browser, and with some exceptions, can do just about anything you can do yourself. They can:
> * Redirect your browser to malicious websites
> * Read your account data (including your account name, and password under certain circumstances)
> * Send your account data to other sites, or the script creator
>
> ⚠️ There have been cases of players losing their account permanently as a result of running malicious scripts - you have been warned!

### How can I spot a malicious script?

> The only sure-fire way to know that a script is malicious is by reading it and understanding what it does. If you aren't sure, you can request help from one of the game developers (anyone with a green name) in the programming channel of the [Bondage Projects Discord][4]. But here are a few things to look out for:

#### Suspicious websites

If you spot URLs or web addresses embedded inside a script, it could be a sign that the script is malicious, unless you recognise the site or are sure it is safe.

#### Deliberately confusing or obfuscated code

If someone goes to lengths to hide what a piece of code is doing, they could be trying to hide malicious code (or they might not know what they're doing, or just be trying to show off). Look out for uses of the `eval` function, and obfuscated strings using the `atob`/`btoa` functions. For example:

```js
eval(atob("UGxheWVyLk5hbWU="))
```

Similarly code that looks like this (known as [JSFuck][5]) is almost certainly trying to hide what it does:

```js
[!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]+[!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]+[!+[]+!+[]+!+[]+!+[]+!+[]+!+[]+!+[]]
```

#### Excessively long scripts

The longer a piece of code is, the more effort it takes to accurately identify what it does. Most basic things in the club can be done in just a few lines of code. If someone sends you a script that's hundreds or thousands of lines long, be cautious, especially if it sounds like it's only doing something simple.

#### The bottom line

If you take nothing else away from this, take this:

> ⚠️ **If you don't know what a script does, don't run it!**

Before running a script, you should always know what it does, or that it comes from a trusted source.

* If you have some coding experience, read the script yourself to verify that it is harmless
* Make sure you trust the source of the script - don't just go running snippets of code that you found in random person's bio
* If you're not sure what a script does or whether it's safe, you can request help from one of the game developers (anyone with a green name) in the programming channel of the [Bondage Projects Discord][4].

---

[1]: https://nordpass.com/most-common-passwords-list/ "NordPass Top 200 passwords list"
[2]: https://haveibeenpwned.com/ "Have I Been Pwned"
[3]: https://en.wikipedia.org/wiki/JavaScript "Wikipedia page: JavaScript"
[4]: https://discord.gg/dkWsEjf "Bondage Projects Discord"
[5]: http://www.jsfuck.com/ "JSFuck"