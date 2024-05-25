# 👋 Hi, I’m @nicfab

- 👀 I’m interested in Privacy, Data Protection, Cybersecurity, and computer science.
- 🌱 I would like to spend more time learning what interests me... and it's so much stuff...

***

# 🧑🏼‍💼 To know something about me:
  - **EN** [About me](https://notes.nicfab.eu/en/pages/about/)
  - **IT** [Chi sono](https://notes.nicfab.eu/it/pages/about/)

***

# 📫 How to reach me:
  
  - **EN**:
    - [**Here**](https://nicfab.linksta.cc)
    - [**How to contact me**](https://notes.nicfab.eu/en/pages/about/#how-to-contact-me)
  - **IT**:
    - [**Qui**](https://nicfab.linksta.cc)
    - [**Come contattarmi**](https://notes.nicfab.eu/it/pages/about/#come-contattarmi)

***

# My WKD
As I wrote in my article entitled "[_Digital identity: Web Key Directory as a possible solution_](https://notes.nicfab.eu/en/posts/wkd/#our-gnupg-public-key)", I decided to set up my own [Web Key Directory (**WKD**)](https://wiki.gnupg.org/WKD) to provide more security and to make it easier to identify the public keys of my email addresses. 

With the tool [**Web Key Directory by Jonatan Miarecki**](https://miarecki.eu/posts/web-key-directory-setup/#online-check) ([Metacode WKD Checker](https://metacode.biz/openpgp/web-key-directory) has been sunsetted on 1.05.2024), it is possible to check whether the WKD system is active for a given email address.

You can verify our email address. 

## My OpenPGP Public Key

You can fetch my public key the following way:

```bash
gpg --locate-external-keys "nicola at myGitHubUsername dot eu"
```
You will find the public key in the response.

If the above command doesn't work due to disabled WKD in `~/.gnupg/gpg.conf` you can run:

```bash
gpg --auto-key-locate clear,wkd --locate-external-keys "nicola at myGitHubUsername dot eu"
```
You can download the public key directly by using the following commands (you can obtain the URL with the tool [**Web Key Directory by Jonatan Miarecki**](https://miarecki.eu/posts/web-key-directory-setup/#online-check) by inputting the email address): 

```bash
curl --tlsv1.3 -o nicfab.eu "https://openpgpkey.nicfab.eu/.well-known/openpgpkey/nicfab.eu/hu/s6wy17ps55re8usymdzz3ghq1z7uefof?l=nicola"
```
or
```bash
wget --secure-protocol=TLSv1_3 --max-redirect=0 -O nicfab.eu "https://openpgpkey.nicfab.eu/.well-known/openpgpkey/nicfab.eu/hu/s6wy17ps55re8usymdzz3ghq1z7uefof?l=nicola"
```

***

_Credits_ [duxsco](https://github.com/duxsco) for the WKD insights.
