---
layout: post
title:  "Encrypt your email with Mailvelope"
date:   2013-06-11 16:20:41
comments: true
categories: security 
---


During last week we've all heard a lot about the previously secret NSA covert surveillance activies. Through the [PRISM surveillance program][prism-wiki], the NSA has at least some access to a lot of user data from many different Internet services, including Google, Facebook, Microsoft, and others.

In addition to this latest revelation, some already-existing laws have the potential affect the privacy of our Internet communications. For example, the ["abandoned email"][eff-abandonded] provision of the [Electronic Communications Privacy Act][ecpa] (ECPA) allows the U.S. government to access emails that have not been read in the last 180 days without probable cause and a warrant. This includes previously read emails that may have been archived or otherwise stored, even in a still-active email account. 

Obviously, this is a little disconcerting; our Internet communication is less significantly less private that we previously thought. 

One of the ways that we can try to protect our privacy is by encrypting email communication. I recently discovered a handy plugin for Google Chrome called [Mailvelope][mailvelope]. Mailvelope seamlessly integrates with the Gmail web interface to provide an easy way to encrypt and decrypt your emails using the OpenPGP standard. (It also seems to support Yahoo and Outlook.com, although I didn't try it with those providers).

When you compose an email and then encrypt it with Mailvelope, the text of the email is replaced with the [ciphertext][ciphertext-wiki]. This means that even if someone (*cough* NSA *cough*) accesses the email from your Gmail account, all they can see is the encrypted message.

When the recipient recieves the email, they will have to decrypt it to see what you sent them. They can either use the Mailvelope plugin also (if they have it installed) or one of many other 3rd-party programs that support OpenPGP messages.

Here's how to set up Mailvelope so that you can send and recieve encrypted emails.

<!-- more -->

Generate Encryption Keys
------------------------

1. Install the Mailvelope plugin (find it in the [Chrome web store][mailvelope-chrome]).

1. Now we have to generate your encryption key. (Mailvelope uses public key encryption, so you encrypt an email to someone with their public key and and they use their private key to decrypt it). Click on the Mailvelope padlock icon (to the right of the Chrome address bar) and choose `Options`.

1. Click the `Generate Key` option on the left side of the options page.

1. Enter your full name, your email address, and a passphrase, and then click submit. IMPORTANT: Choose a strong, secure passphrase. You will use this passphrase to unlock your private key so that you can decrypt emails sent to you.

1. Click `Display Keys` on the left side of the options page. This will show the list of keys you have available. At this point, the only key that'll be visible is the key we just generated. Notice the icon that looks like two keys. This means that you have both the public and private keys for this keypair. If the icon is a single key, that means that you only have the public key, allowing you to encrypt an email for someone else to read.


Exchanging Public Keys
----------------------

1. To send an encrypted email to someone, you're going to need their public key. For them to respond, they will need yours. It's totally safe to send a public key by any means - in fact,  you should publicize it as much as possible so that it's easy for someone to send you an encrypted email. (If you want to send *me* an encrypted email, you can find my public key [here](/blog/2013/06/08/openpgp-key/).)

1. To display your public key in Mailvelope, click the `Export` dropdown menu, and choose `Display public key`. This is the key you want to share.

1. Once you have someone else's public key, click `Import Keys` in the Mailvelope options page. You can simply paste their key (including the `-----BEGIN PGP PUBLIC KEY BLOCK-----` and `-----END PGP PUBLIC KEY BLOCK-----` lines) into the text box and click submit.

1. Click `Display Keys` again. Notice that the new public key has been added. 


Send An Encrypted Email
-----------------------

1. Now open your Gmail account and begin to compose a new email. You can fill out the recipient's email address and subject (remember not to put any sensitive/private information in the subject; it's not encrypted).

1. Click the icon that appears when you mouse over the compose area. It looks like a notepad with a yellow pencil. This will bring up the secure compose window.

1. Compose your email. When you have finished writing it, click the yellow padlock button. You will be prompted to choose who to encrypt the email for. The dropdown menu has a list of all the keys you have. Choose the name/email address of the person who's public key you imported earlier, and click the "Add" button. 

1. Click `Ok`. The plaintext email you wrote will be replaced with the encrypted email (starting with the line ` -----BEGIN PGP MESSAGE-----  ` ). 

1. Click `Transfer`. This puts the encrypted message into the Gmail compose window.

1. Click send. That's it! You just sent an encrypted email.


Decrypting Recieved Email
-------------------------

Now, assuming this worked, the person you sent the encrypted email to has responded with another message, this time encrypted with *your* public key. You will have to use the private key we generated earlier to decrypt it.

1. Open the encrypted email that was sent to you in the Gmail web interface. When you hover over the contents of the encrypted message, Mailvelope will show a padlock icon hovering over the message text. 

1. Assuming that the person who sent the email encrypted it with your public key, Mailvelope will prompt you to enter the passsphrase for your private key. This is the passphrase you chose when you generated your keypair.

1. Enter your passphrase and click `Ok`. The decrypted secret message will be displayed. That's it!


Hopefully you now know how to send and recieve encrypted emails. This obviously won't help with other Internet communications, i.e. via Facebook, Twitter, etc. You'll just have to avoid using those platforms for communications of a...sensitive nature :). 


[prism-wiki]: http://en.wikipedia.org/wiki/PRISM_(surveillance_program)
[eff-abandonded]: https://ssd.eff.org/book/export/html/42#node-46
[ecpa]: http://en.wikipedia.org/wiki/Electronic_Communications_Privacy_Act
[mailvelope]: http://www.mailvelope.com
[ciphertext-wiki]: http://en.wikipedia.org/wiki/Ciphertext
[mailvelope-chrome]: https://chrome.google.com/webstore/detail/mailvelope/kajibbejlbohfaggdiogboambcijhkke
