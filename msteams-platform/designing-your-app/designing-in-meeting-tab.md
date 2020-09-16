---
title: Designing the Microsoft Teams meeting in-meeting tab
author: heath-hamilton
description: Guidance and best practices for designing the in-meeting tab for Microsoft Teams.
ms.author: lajanuar
ms.topic: conceptual
---
# Designing an in-meeting tab

The in-meeting tab is a canvas for augmenting collaboration during meetings. Based on the Teams tab capability, attendees can see and interact with app content in a dedicated space outside the meeting stage through shared or role-based views.

## Use cases

People might use the in-meeting tab during meetings to:

* Submit detailed feedback (for example, evaluate a job candidate)
* Quickly create a poll, survey, or task item for the meeting participants
* Display notes relevant to the meeting (for example, information about a sales lead)

## Example

The following example shows the in-meeting tab displaying survey app content during a meeting.

:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-organizer-view.png" alt-text="Example shows what the meeting in-meeting tab might look like from a meeting organizer's perspective.":::

<a href="https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=208%3A9816" target="_blank">See the full scenario (Figma)</a>

<a href="https://www.figma.com/file/cqL4AfKxnjKYjcv5jbgfMv/Principles-and-guidelines?node-id=97%3A0" target="_blank">See other example use cases (Figma)</a>

## Anatomy

The in-meeting tab is a Teams tab that displays content with the following dimensions:

* **Width**: 280 pixels (with 20 pixels of padding on either side)
* **Height**: Full bleed to the bottom of the in-meeting tab. There are 20 pixels of padding between the pane header and the webview.

:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-anatomy.png" alt-text="Illustration showing the UI anatomy of a meeting extension in-meeting tab." border="false":::

1. **App icon**: The entry point to the in-meeting tab.
1. **in-meeting tab header**: Includes tab name, more actions, and dismiss button.
1. **Tab name**: The name of the tab instance.
1. **More actions**: Provides options on hover that include:
   * Reload the tab.
   * Rename the tab.
   * Mute notifications from the app during the meeting.
   * Open app settings and About dialog.
   * Remove the tab from the meeting.
1. **Dismiss**: Dismisses the in-meeting tab. Always use the upper-right close icon instead of an action in the footer.
1. **Webview**: Displays all third-party app content.

## Behavior

### Scrolling

Here's what to know about scrolling in the in-meeting tab:

* You should only be able to scroll vertically.
* You can only see the content you've scrolled to (nothing above or below).
* The scrollbar is part of the webview content.

:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-scroll.png" alt-text="Illustration showing how scrolling the webview content in the in-meeting tab works." border="false":::

### Navigation

For scenarios with navigation layers or heavy content, we recommend allowing users to navigate to a secondary layer. Users must be able to go back to the previous layer.

:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-nav.png" alt-text="Illustration showing how navigating to a secondary layer in the in-meeting tab works." border="false":::

## Components

In-meeting tabs are built primarily with the following UI components (which are based on the [Fluent Design System](https://fluentsite.z22.web.core.windows.net/)).

Component | Guidelines | Example
 - | - | -
[Button](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10089) | Primary and secondary buttons can be medium or small | Send a response
[Input](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10102) | Field for brief user input. Label text can include an icon  | Enter feedback
[Dropdown](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10115) | Select one or more options from a list. Can include search and multi-selection features | Choose a language
[Selection controls](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10128) | Use checkboxes for multiple choices or radio buttons and toggles for single choices. For more detailed selections, use a slider | Vote in a poll
[Alerts](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10141) | Whether displaying an urgent message, error state, or warning, the message should be short and won't interrupt the user's current task | Display issue when submitting a response

## Theming

### Colors

Use the [recommended color scheme](https://www.figma.com/file/cqL4AfKxnjKYjcv5jbgfMv/Principles-and-guidelines?node-id=280%3A3102) for backgrounds, foregrounds, and conveying states in meeting notification modals.

[See the full color scheme](https://www.figma.com/file/cqL4AfKxnjKYjcv5jbgfMv/Principles-and-guidelines?node-id=257%3A15339)

### Typography

Use the [recommended font sizes and weights](https://www.figma.com/file/cqL4AfKxnjKYjcv5jbgfMv/Principles-and-guidelines?node-id=258%3A16040) for titles, body text, and metadata text.

## Best practices

### Responsiveness

In-meeting tab layouts should be able to scale to various sizes. Consider how the tab will scale and take shape before, during, and after the meeting.

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-before-meeting.png" alt-text="Illustration showing that the in-meeting tab content looks like a full-screen tab before and after a meeting." border="false":::

#### Before the meeting

Make sure your tab layout can adapt to a right to left layout for different languages and that controls move to the right locations. (This layout could also apply to after the meeting.)

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-during-meeting.png" alt-text="Illustration showing how the pre-meeting tab content is condensed to the in-meeting tab during a meeting." border="false":::

#### During the meeting

Tab content moves to the in-meeting tab.

   :::column-end:::
:::row-end:::

### Theming

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-theming-do.png" alt-text="Illustration showing how you should design the in-meeting tab for the dark theme used in Teams meetings." border="false":::

#### Do: Design for a dark theme

Teams meetings are optimized for dark mode to help reduce visual and cognitive noise so users can focus on the discussion and shared content.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-theming-dont.png" alt-text="Illustration showing you shouldn't use colors that aren't conducive to the Teams dark theme." border="false":::

#### Don't: Use unfamiliar colors

Colors that clash with the meeting environment may be distracting and appear less native to Teams.

   :::column-end:::
:::row-end:::

### Scrolling

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-scroll-do.png" alt-text="Illustration showing you should only allow vertical scrolling in the in-meeting tab." border="false":::

#### Do: Scroll vertically

Users anticipate vertical scrolling in Teams (and elsewhere).

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-scroll-dont.png" alt-text="Illustration showing showing you shouldn't allow horizontal scrolling in the in-meeting tab." border="false":::

#### Don't: Scroll horizontally

Horizontal scrolling isn’t an expected behavior in Teams. Other canvases in the meeting environment scroll vertically.

   :::column-end:::
:::row-end:::

### Layout

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-layout-do.png" alt-text="Illustration showing the recommended single-column layout in the in-meeting tab." border="false":::

#### Do: Single columns

Given the in-meeting tab’s narrow nature, we strongly recommend displaying the contents in a single column.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-layout-dont.png" alt-text="Illustration showing how a two-column layout in the in-meeting tab isn't ideal." border="false":::

#### Don't: Multiple columns

Due to the limited space of the in-meeting tab, layouts with more than one column aren’t recommended.

   :::column-end:::
:::row-end:::

### Navigation

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-nav-do.png" alt-text="Illustration showing you should always provide a back button if your in-meeting tab app has more than one layer of navigation." border="false":::

#### Do: Have a back button

If you have more than one layer of navigation, users must be able to go back to their previous view.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-nav-dont.png" alt-text="Illustration showing that adding another close button in the in-meeting tab for navigation is redundant and could cause issues." border="false":::

#### Don't: Include another close button

Providing an option to close in-meeting tab content may cause issues since there’s already a close button in the header to dismiss the in-meeting tab itself.

   :::column-end:::
:::row-end:::

:::row:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-tab-nav-caution.png" alt-text="Illustration showing that you need to be cautious when using modals (i.e., task modules) in the in-meeting tab given the limited space." border="false":::

#### Caution: Using dialogs in a narrow space

Dialogs, such as task modules, in the already narrow in-meeting tab might wrap the content and obscure the information.

   :::column-end:::
:::row-end:::

## Accessibility

For information on accessibility, see [Figma](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=1263%3A16).

## Resources

* [Meeting extensions Figma file](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=254%3A35598)

## Validate your design

If you plan to publish your app to AppSource, you should understand what design issues commonly cause apps to fail during submission.

> [!div class="nextstepaction"]
> [Check design validation guidelines](https://review.docs.microsoft.com/en-us/microsoftteams/platform/concepts/deploy-and-publish/appsource/prepare/frequently-failed-cases?branch=restructure-design-topics-ia#validation-guidelines)
