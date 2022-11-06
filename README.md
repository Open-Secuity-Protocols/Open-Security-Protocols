# Open-Security-Protocols
Best Security practices for anyone cautious about their privacy to remain secure on the internet.

## Mobile Security
### Search Engines

- On mobile, don't use proprietary search engines such as `Google Chrome`.
- Instead, you shoud install and use `DuckDuckGo` as your primary search engine.
- It's available on all mobile platforms.

### Setting up DuckDuckGo
---

- [x] After installing the app, perform the following changes.
- [x] Enable `App Tracking Protection` globally, this will block tracking requests on your apps.
- [x] Enable delete history and cookies on app closed.
- [x] Set up your `@duck.com` email address to mask you real email addresses, this will remove trackers that are normally added to your emails. Emails will be sent and received with your actual email.
- [x] Disable search suggestions if you hate it.

---

### VPN and AD Blocking
---

- For the case of using a VPN, I strongly condemn using a VPN that you don't own, this means that you need to run your own `private VPN` that you have control over.
- A majority of VPN's actually do track you almost all the time.
- They claim that they do not keep any logs yet some of them do keep logs and even submit them to law enforcement if they are summoned to do so.
- I will talk about how you can set up one and be able to connect it from anywhere.
- What we are going to set up here is a service that combines a `VPN`, a `DNS service` and an `AD blocker` all in one.
- This will be a bit technical but its worth it.

---

### Setting up the Service
---

- [x] You first need to get a `virtual machine`, preferably on any Cloud provider of your choice.
- [x] You don't need to pay for the machine since a majority of the providers always have services that are free forever. In this case, we will use `Oracle Cloud`.
- [x] Sign Up on the platform.
- [x] Select a region where you want it to be provisioned then proceed to spin up a virtual machine that is `free forever`.
- [x] This will come with `1GB RAM` and `1 CPU`. This should be enough for personal use.
- [x] Choose `Ubuntu` as your OS since it easier to set up on this one.
- [x] Ensure that you have generated an `SSH Public key and Private key pair` then add the public key during the set up process.
- [x] Once it has been provisioned, grab its IP address then SSH into it.
- [x] Should be something like this.
```bash
    ssh ubuntu@<machine-ip-adddress>
```
- [x] Go ahead and update packages.
```bash
    sudo apt update && sudo apt upgrade
```
- [x] Once done, proceed to install `Docker` and `Docker Compose`.
- [x] You should follow the guide here to do that [Docker-Installation]("https://docs.docker.com/compose/install/linux/")