# 🔘 Radio Button Group Component

A **Radio Button Group** lets users select **one option** from a list of predefined choices. This component is ideal for scenarios where a single, clear selection is required.

---

## ✨ Overview

A **radio button group** is a UI pattern that presents several related options as **rounded buttons**, typically arranged horizontally. Only **one button** in the group can be selected at a time, helping users make confident and intentional decisions.

---

## 🎯 Use Case

Use this component when:
- You need users to **select only one option** from a predefined list.
- You want to **guide users toward a clear choice**.
- You want to avoid checkboxes or dropdowns when the number of options is small.

---

## 🧩 Features

- Clean, modern UI with **rounded buttons**.
- **Horizontal layout** for easy readability.
- Reactivity: shows the **selected value** instantly.
- Fully customizable and accessible.

---

## 🖼️ Example Preview
# 🔘 Radio Group Component – Two Styles: Radio & Button

This project showcases the use of **radio groups** in Salesforce Lightning Web Components (LWC), supporting two styles:

1. **Standard Radio Buttons** – Traditional circular selection
2. **Button-style Radio Group** – Stylish toggle-button appearance using `type="button"`

Only one option can be selected at a time.

---

## 🧩 Component Example

Here's how you define a radio group in LWC using the `lightning-radio-group` base component:

```html
<template>
  <lightning-radio-group
    name="radioGroup"
    label="Radio Group"
    options={options}
    value={value}
    type="button"> <!-- or type="radio" for standard style -->
  </lightning-radio-group>
</template>

// radioGroups.js
// This LWC class defines the logic for a radio button group component

import { LightningElement } from 'lwc';

export default class RadioGroups extends LightningElement {
    // Holds the currently selected value from the radio group
    value = '';

    // Getter that returns the list of options to be displayed in the radio group
    get options() {
        return [
            { label: 'Sales', value: 'option1' },  // First option
            { label: 'Force', value: 'option2' },  // Second option
        ];
    }
}


| Property  | Description                                                     |
| --------- | --------------------------------------------------------------- |
| `name`    | A unique name for the group (backend)                                 |
| `label`   | The label displayed above the group (ui)                           |
| `options` | Array of `{ label, value }` objects   (ui)                          |
| `value`   | The currently selected value(not displayed until selected)                                  |
| `type`    | `"radio"` (default) for circular inputs, `"button"` for buttons |




