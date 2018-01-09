# Instagram Widget

This guide is oriented for Shopify Stores but can be easily adapted.

## Install
Create a snippet called 'instagram-feed', and add the following script to your theme.
```
{{ 'jquery.instagram.js' | asset_url | script_tag }}
```

Here is a basic configuration:
```
<div id="instafeed" data-access-token="{{ settings.insta_token }}" data-user-id="{{ settings.insta_id }}"></div>

<script>
    var insta = document.getElemendById('instafeed')

    var feed = new Instafeed({
        get: 'user',
        userId: insta.getAttribute('data-user-id'),
        accessToken: insta.getAttribute('data-access-token')
    });
    feed.run();
</script>
```

On the settings-schema.json file add a section called 'Instagram Feed' with the following settings:
```
    {
      "type": "text",
      "id": "insta_token",
      "label": "Access Token"
    },
    {
      "type": "text",
      "id": "insta_id",
      "label": "User ID",
      "info": "If it's your account, it's the string before the first dot (.) on the Access Token."
    }
```

## Example Design

The above is a basic example of how to use it. We have provided a sample snippet and some css you can copy and modify for your store. Make sure the grid classes match your theme.

## Inquiries
Any questions, let us know at: support@pasilobus.com.
Please report bugs by filing a new issue.

Learn more about Pasilobus at our website https://www.pasilobus.com
