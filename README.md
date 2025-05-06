# Eye One Accessibility Widget – GTM Template

This repository contains a Google Tag Manager **Community Template** for the **Eye One Accessibility Widget** (the “All in One Accessibility” overlay). Use this template to easily embed the accessibility widget on your website via GTM, without needing to manually add code to your site.

## Usage

1. **Install the Template:** Import the template into your Google Tag Manager workspace. You can do this by searching the Community Template Gallery for "Eye One Accessibility Widget" and clicking **Add to Workspace**, or by importing the `template.tpl` file in GTM’s Templates section.

2. **Add your API Key:** Obtain your Eye One Accessibility **API key** (license key) from your Eye One/All-in-One Accessibility account. In GTM, create a new **Tag** and select the *Eye One Accessibility Widget* template. In the tag settings, you will see a field for **API Key** – paste your key string there.

3. **Configure Trigger:** Typically, you should fire this tag on **All Pages** (so the widget loads on every page of your site). Add an appropriate trigger (e.g. DOM Ready or Page View – All Pages) to the tag.

4. **Save and Publish:** Save the tag configuration. Submit and publish your GTM container. Once published, the Eye One Accessibility widget script will be injected on your site’s pages, and the widget should appear (usually as an accessibility icon interface).

## How it Works

- The template uses GTM’s sandboxed JavaScript APIs to inject the widget. It sets a global variable with your API key and then loads the widget’s script from Eye One’s servers.  
- On successful load, the widget is initialized on your site (visitors can then use the accessibility toolbar provided). The tag signals success via `gtmOnSuccess()` – if the script fails to load, `gtmOnFailure()` is invoked, so you’ll see an error in GTM’s preview/debug mode.

## Customization

This template simply loads the widget. All customization of the widget (appearance, features) should be done via the Eye One Accessibility dashboard or configuration provided by the service, not in GTM. Ensure the API key used is correct and corresponds to your domain (the widget may not load if the key is invalid or not authorized for your site).

## Support

For issues with the template, you can open an issue in this repository’s [Issues](../issues) section. For issues with the widget service itself (e.g., questions about accessibility features or the widget’s behavior), refer to [Eye One Accessibility’s support](https://www.eyeoneaccessibility.com/support) or documentation.

## License

This template is provided under the Apache 2.0 License (see [LICENSE](LICENSE) file for details).
