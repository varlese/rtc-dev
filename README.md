# righttocounsel.github.io
Right to Counsel Campaign Site

## Creating new posts
To create a new post, go to `content > posts`. You can use `example-post.en.md` as a template for posts in English, and `example-post.es.md` for posts in Spanish.

To create a new post, create a new file in the `posts` folder and make sure it ends with `en.md` (for English) or `es.md` (for Spanish). Then, copy the text from the example posts and update the content, title, etc. When you're finished, add and commit the new file.

## Creating new pages
To add a new page to the site, create a new `en.md` or `es.md` file in the `content` folder. 

## Updating the homepage content
The homepage template is set via `layouts > partials > home-intro.html`. 

To update the static text that appears on the homepage, visit `data > en > homepage.yaml`. 

To translate the static text that appears on the homepage, duplicate this file in a language folder. For example, creating the translation in `data > es > homepage.yaml` will display the Spanish version of the homepage text on the `es` version of the site. 

## Changing the menu
To update items in the English menu, visit `data > en > nav.yaml`.

To update items in the Spanish menu, visit `data > es > nav.yaml`. 

## Updating social links
The social links are automatically populated to the site using the `social.yaml` file.

To update, visit `data > en > social.yaml` and update the URL next to the social media site you want to link to. Lines with a `#` in the beginning are deactivated. To reactivate them, remove the hashtag and update the URL. The icons will automatically appear on the front-end of the site.

## Shortcodes

### Embedding Action Network signups
Action Network provides a shortcode that you can use on the site to embed the sign-up forms. To use these with the Right to Counsel website, visit `layouts > shortcodes > action-network-form.html`. 

In `action-network-form.html`, copy and paste the code from Action Network. This will create a custom shortcode for the sign-up form.

To embed the sign-up using this new shortcode, paste the following on the page where you'd like the form to appear:
`{{< action-network-form >}}`

### Buttons
The button shortcode is set up via `layouts > shortcodes > button.html`. To use a button on the site, use this shortcode:
`{{< button link="URL" text="Link Text" target="_blank" >}}`

## Translation
Different languages can be enabled in `config.toml`. Once the language is enabled, you can:
- Add new posts or pages by specifying the language shortcode in the file extension, i.e. `es.md` or `fr.md`
- Add new partial layouts, such as an intro, navigation bar, footer, via the related language folder in the `data` folder, i.e. `data > es`.
- Update the contact form by creating a related `.toml` file under `i18n`, copying the base `en.toml` file format.

