title: DevTools Tutorial

# Chrome Dev Tools aka Inspect Element

## Network

### The Basics

For a very basic tutorial on how to use the network tab, see [here](https://developers.google.com/web/tools/chrome-devtools/network#open).

!!! Tip
    If your Google Chrome does not work, you can switch to a different browser such as Microsoft Edge. Sometime Inspect Element will not work if you are logged into your YRDSB email when using the browser.

### How to Use

!!! success "Always read the official documentation!"
    This is just a *very basic* run-down of the [Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools). For more information, see the official Chrome DevTools documentation. Their beautifully written documentation covers more in-depth topics. [Click here](https://developers.google.com/web/tools/chrome-devtools/network/reference) for their reference!

1. Click on an entry to bring it up. The entries, by default, are sorted downwards by time (the bottom-most entry will be the most recent request).<br /><br />
![](/Images/Inspect3.png)
2. Take note of important fields:<br /><br />
![](/Images/Inspect4.png)
3. You should see 6 tabs: Headers, Preview, Response, Timing, Cookies and Initiator.
    - Under the **Headers** tabs, you should see the complete HTTP request *and* response being sent/received. Especially take note of the values under the **General** and **Query String Parameters** sections. Under the **Request Headers** section, watch out for the `Content-Type` field (if it exists).
    
    !!! note
        During a `POST` request, if the `content-type` is `application/x-www-form-urlencoded`, then you will see a **Form Data** section instead of a **Query String Parameters**.
    !!! tip
        Since Chrome nicely interprets the data for you, you can click "View Source" to see the raw data being sent:
        ![](/Images/Inspect5.png)  
        Can you guess what the source of the above data would be? That's right! It's `username=aa&password=bb`
    - Under the **Preview** tab, you should see the human-readable formatted/parsed response from the server. If the response is in JSON, then Chrome will format it into a tree/accordion. If the response is a HTML document, the Chrome will render the document for you. Here's an example of a formatted JSON preview:<br /><br />
    ![](/Images/Inspect6.png) 
    - Under the **Response** tab, you should see the raw unformatted data that the server sent back.
    - Under the **Cookies** tab, you should see all the cookies the server sent back.

### Life Hacks

You can open the Inspect Element window with the shortcut `Ctrl-Shift-I` on PC.

!!! warning
    When the website refreshes, you will loose all your previous logs (and possibly important information).

To avoid this, click `Preserve Log` (as shown below):  

![](/Images/Inspect0.png)

!!! danger
    When your logs become too messy, you should clear it to avoid confusing yourself!

To clear your logs, click the "Clear" button:  

![](/Images/Inspect1.png)

Click on the "Filter" icon to bring up the possible filter options. Sometimes, you may wish to find only particular queries. For example, you can filter out everything except XHR (XmlHttpRequests) by clicking the "XHR" button.

![](/Images/Inspect2.png)

## How to View/Edit/Delete Stored Cookies

!!! success "Always read the official documentation!"
    There's no use to writing anything if you can just see a better version [here](https://developers.google.com/web/tools/chrome-devtools/storage/cookies)!

## But I use Firefox!
Well, you're in luck my friend. Just like Chrome, Mozilla has very detailed documentation on their [DevTools here](https://developer.mozilla.org/en-US/docs/Tools).

!!! example "I want to see the network tools!"
    For a general overview, see [here](https://developer.mozilla.org/en-US/docs/Tools/Network_Monitor).  
    To learn about deciphering request details, click [here](https://developer.mozilla.org/en-US/docs/Tools/Network_Monitor/request_details).  
    To learn about the network request list, click [here](https://developer.mozilla.org/en-US/docs/Tools/Network_Monitor/request_list).

!!! example "What about cookies?"
    You thought I forgot? [No way!](https://developer.mozilla.org/en-US/docs/Tools/Storage_Inspector#Cookies)

!!! note
    Mozilla has categorized their DevTools into two distinct categories: "Core Tools" and "More Tools". If you can't find something, be sure to check both categories!

## But I use Edge!
I hope that by now, you've learned to [read the documentation](https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide).

## But I use Safari!
Again, [read the documentation](https://support.apple.com/en-ca/guide/safari-developer/welcome/mac). Just saying, the Apple documentations suck. Why don't you try [Chrome](https://www.google.com/chrome/)?

## But I use [insert some random browser here]!
Why don't you try Googling "[some random browser] devtools documentation". You're bound to find *something*.
