---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Integration Modules

The d>sponsor platform offers out-of-the-box integration modules to facilitate ad displays, while allowing for advanced customization to meet the specific needs of media and creators.

### Integrations are available through the admin interface at admin.dsponsor.com

* _**HTML Widget**_: A ready-to-use component, with no external JavaScript or CSS dependencies, designed for easy integration into any web page or email. Simply copy and paste to insert a clickable logo panel or dynamic banner.&#x20;
* _**Dynamic banner image URL**_: This stable URL points to an image that automatically updates and randomly scrolls through pre-validated ads. It's an efficient way to diversify ad impressions without requiring the publisher to change the embedded URL on their content platform.

### Development of new modules

#### _Integration and interaction methods with d>sponsor_

There are several ways to create custom modules for displaying advertising data.&#x20;

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

#### _Data Specifications_

The following data format is recommended, but not required:

```
{
  "property_payload_type": "string", // identifier of the ad format
  "property_payload_version": "string", // version following the SemVer convention
  "content": "Object" // object containing ad data
}
```

Such a JSON format can be stored on IPFS. The corresponding CID is provided to the DSponsor.sol contract, allowing the integration module to retrieve the content via IPFS.

* Example for the clickable logo insert:

```
{
  "property_payload_type": "ClickableLogo",
  "property_payload_version": "1.0.0",
  "content": {
    "logo": "https://example.com/logo.jpg",
    "link": "https://example.com/?utm_source=dsponsor"
  }
}
```

* &#x20;Example for the dynamic banner:

```
{
  "property_payload_type": "DynamicBanner",
  "property_payload_version": "1.0.0",
  "content": {
    "image": "https://example.com/banner.jpg",
    "text": "<p>Your custom text here with <a href='https://example.com/?utm_source=dsponsor'>link</a>.</p>"
  }
}

```

#### _Data Validity_&#x20;

Integration modules must include verification mechanisms to ensure that the data they receive is compliant. For example, ensuring that images are square or that HTML content does not contain potentially malicious elements. These measures are essential to ensure that advertisements meet the quality and safety standards required by broadcast platforms, while maintaining the integrity of the user experience.
