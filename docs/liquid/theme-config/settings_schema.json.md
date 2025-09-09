# settings\_schema.json

---
  The settings_schema.json file controls the organization and content of the
  Theme settings area of the theme editor. All setting selections in the theme
  editor are saved in settings_data.json.
---

## **Defining a theme setting**

The structure of the settings definitions in settings\_schema.json is as follows:

* Each settings entry contains definitions for individual settings.
* Each individual setting has a few attributes, which vary depending on whether the setting is for merchant input or sidebar styling.

Here's an example of a settings definition in the settings\_schema.json file:

```
{
    "theme": "Shopcada Super Theme",
    "option_groups": [
        {
            "label": "General",
            "options": [
                {
                    "label": "Colours",
                    "type": "group",
                    "options": [
                        {
                            "type": "color",
                            "label": "Primary Color",
                            "id": "color_primary"
                        },
                        {
                            "type": "color",
                            "label": "Secondary Color",
                            "id": "color_secondary"
                        }
                    ]
                },
            ]
        }
    ]
}
```

#### Output
![](<../../assets/images/documents/image (68).png>)

[cashback](liquid/variables/cashback.md)

## JSON Format

| Attribute | Required? | Description |
|-----------|-----------|-------------|
| type      | yes       | Name of the settings type. |
| id        | yes       | The unique name for this setting. The id is exposed to the liquid templates via the settings object. It must only contain alphanumeric characters, underscores, and dashes. |
| label     | yes       | A label for this setting. |
| default   | no        | A value to which the setting can default. |
| info      | no        | Additional information about the setting. Use sparingly, as it's better to use only informative labels whenever you can. |
| options   | no        | Options for the fields (radio, select, checkbox) with label and value. |



## Input Settings

<table>
    <thead>
        <tr>
            <th>Value</th>
            <th>Application</th>
            <th>Example</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>text</td>
            <td>Single-line text fields</td>
            <td>
                <pre>
					{
						"label": "Slide title",
						"type": "text",
						"id": "slide_1_title"
					}
                </pre>
            </td>
        </tr>
        <tr>
            <td>textarea</td>
            <td>Multi-line text areas</td>
            <td>
                <pre>
					{
						"type": "textarea",
						"id": "copyright_text",
						"label": "Copyright text",
						"default": "Copyright © 2020 your site name"
					}
                </pre>
            </td>
        </tr>
        <tr>
            <td>image_picker</td>
            <td>Image uploads</td>
            <td>
                <pre>
					{
						"label": "Logo",
						"type": "image_picker",
						"id": "logo_img",
						"default": "",
						"info": "450 x 200px recommended"
					}
                </pre>
            </td>
        </tr>
        <tr>
            <td>radio</td>
            <td>Radio buttons</td>
            <td>
                <pre>
					{
						"type": "radio",
						"id": "radio_id",
						"label": "Radio Text",
						"options": [
							{
								"value": "one",
								"label": "Radio one"
							},
							{
								"value": "two",
								"label": "Radio two"
							}
						],
						"default": "one"
					}
                </pre>
            </td>
        </tr>
        <tr>
            <td>select</td>
            <td>Selection drop-downs</td>
            <td>
                <pre>
					{
						"type": "select",
						"label": "Size",
						"id": "body_font_size",
						"default": "13px",
						"options": [
							{
								"value": "12px",
								"label": "12px"
							},
							{
								"value": "13px",
								"label": "13px"
							},
							{
								"value": "14px",
								"label": "14px"
							}
						]
					}
                </pre>
            </td>
        </tr>
        <tr>
            <td>checkbox</td>
            <td>Checkboxes</td>
            <td>
                <pre>
					{
						"type": "checkbox",
						"id": "sticky_header",
						"label": "Enable Sticky Header"
					}
                </pre>
            </td>
        </tr>
        <tr>
            <td>range</td>
            <td>Range sliders</td>
            <td>
                <pre>
					{
						"type": "range",
						"id": "font_size_id",
						"min": 12,
						"max": 18,
						"step": 1,
						"unit": "px",
						"label": "Font size",
						"default": 16
					}
                </pre>
            </td>
        </tr>
        <tr>
            <td>number</td>
            <td>Html5 number</td>
            <td>
                <pre>
					{
						"label": "Logo width",
						"type": "number",
						"id": "logo_width",
						"default": "200"
					}
                </pre>
            </td>
        </tr>
        <tr>
            <td>color</td>
            <td>Color picker</td>
            <td>
                <pre>
					{
						"type": "color",
						"label": "Color",
						"id": "body_text_color",
						"default": "#333333"
					}
                </pre>
            </td>
        </tr>
        <tr>
            <td>group</td>
            <td>Group of settings</td>
            <td>
                <pre>
					{
						"label": "General",
						"options": [
							{
								"label": "Body text",
								"type": "group",
								"options": [
									{
										"type": "select",
										"id": "body_font_family",
										"label": "Font",
										"default": "Georgia,'Hoefler Text', 'Times New Roman', serif",
										"options": [
											{
												"value": "'Rajdhani','HelveticaNeue', 'Helvetica Neue', sans-serif",
												"label": "Rajdhani"
											},
											{
												"value": "'Avant Garde', Avantgarde, 'Century Gothic', CenturyGothic, 'AppleGothic', sans-serif",
												"label": "Avant Garde"
											}
										]
									}
								]
							}
						]
					}
                </pre>
            </td>
        </tr>
    </tbody>
</table>

