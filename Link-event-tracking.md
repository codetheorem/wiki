### What is it?

In order to track links, we use event tracking. Google Tag Manager (GTM) takes care of firing the Google Analytics (GA) script when a click event happens. Then, the information for that link is sent. 

There are many ways GTM can gather information from a link, but in our case, we're using the HTML 5 `data-` attribute tag. This allows us to send information to GA that is relevant to us. 

### How does event tracking work in EOS?

Google Analytics events are usually structured in the following way:
* **Event category:** Typically the object that was interacted with (e.g. 'Video')
* **Event action:** The type of interaction (e.g. 'play')
* **Event label:** Useful for categorizing events (e.g. 'Fall Campaign')

Since our current focus is tracking links, we've set up our data attributes the following way:
* **Event category:** This is where we define the type of link: 'Dropdown link', 'External link', 'Internal link'
* **Event action:** Here we explain the link action: 'Specifications', 'XD Design'...
* **Event label:** Here we give context. Where is this link located ('Alerts', 'Buttons', 'Colors'...)

### Code structure
Here is an example of how the `data-` attribute tag is used to track a link:

```
a(href='https://xd.adobe.com/spec/32746485-3e9f-4bf0-5592-d0551ff56c9c-4445/', data-event-category='Dropdown link', data-event-action='Specifications', data-event-label='Alerts', target='_blank')
    i.eos-icons.md-18
      | open_in_new
    | Design specifications
```

### How GTM handles events
There are three elements in GTM: Variables, Triggers & Tags.

**Variables**

This is where we tell GTM what data we want to capture & send to Analytics. This is the data we've added in the `data-` attribute tag. In the case of the `data-event-action` attribute we've specified before, it would look like this:

![variable](uploads/d71d13daa26bd4e66b0ed08d61992911/variable.png)

**Triggers**

Next we need to tell GTM when to trigger the loading of the analytics tag. GTM is listening to all events but only when a link includes a specific `data-event-` attribute it should trigger. Something else we need to consider in the case of EOS is that this should only happen if the user has previously accepted the privacy policy and a confirmation cookie is present in the browser:

![trigger](uploads/7a038d46949e633eb2866e064b3b9428/trigger.png)

**Tags**

The trigger loads a tag whic takes care of sending the data present in all the `data-event-` attributes. It also maps it to GA's event structure: Category, Action & Label:

![tag](uploads/65f3e1bb05a77ad6c8e40509b9b55df1/tag.png)


### Events in GA
This how these events will appear in Google Analytics:

![Screenshot_2019-11-06_at_14.16.04](uploads/684f9a44c3298ac997ff43e17f734c74/Screenshot_2019-11-06_at_14.16.04.png)

If we drill down in an action, we'll see the label where we'll find out where the link is placed:

![Screenshot_2019-11-06_at_14.16.14](uploads/a56312bd2e86a1dbc3817c8ea3b7fd5d/Screenshot_2019-11-06_at_14.16.14.png)
