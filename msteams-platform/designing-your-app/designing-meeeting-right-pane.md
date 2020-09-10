---
title: Designing the Microsoft Teams meeting right pane
author: heath-hamilton
description: Guidance and best practices for designing the meeting right pane for Microsoft Teams.
ms.author: heath-hamilton
ms.topic: conceptual
---
# Designing the meeting right pane

The right pane is a canvas for augmenting collaboration during meetings. Based on Teams tabs, attendees can see and interact with app content in a dedicated space outside the meeting stage through shared or role-based views.

## Use cases

People might use the right pane during meetings to:

* Submit detailed feedback (for example, evaluate a job candidate)
* Quickly create a poll, survey, or task item for the meeting participants
* Display notes relevant to the meeting (for example, information about a sales lead)

## Example

The following example shows the right pane displaying survey app content during a meeting.

:::image type="content" source="../assets/images/calls-and-meetings/right pane-organizer-view.png" alt-text="Example shows what the meeting right pane might look like from a meeting organizer's perspective.":::

<a href="https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=208%3A9816" target="_blank">See the full scenario (Figma)</a>

<a href="https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=218%3A10461" target="_blank">See other example use cases (Figma)</a>

## Anatomy

The right pane is a Teams tab that displays content with the following dimensions:

* **Width**: 280 pixels (with 20 pixels of padding on either side)
* **Height**: Full bleed to the bottom of the right pane. There are 20 pixels of padding between the pane header and the webview.

:::image type="content" source="../assets/images/calls-and-meetings/right-pane-anatomy.png" alt-text="Illustration showing the UI anatomy of a meeting extension right pane." border="false":::

1. **App icon**: The entry point to the right pane.
1. **Right pane header**: Includes tab name, more actions, and dismiss button.
1. **Tab name**: The name of the tab instance.
1. **More actions**: Provides options on hover that include:
   * Reload the tab.
   * Rename the tab.
   * Mute notifications from the app during the meeting.
   * Open app settings and About modal.
   * Remove the tab from the meeting.
1. **Dismiss**: Dismisses the right pane. Always use the upper-right close icon instead of an action in the footer.
1. **Webview**: Displays all third-party app content.

## Behavior

### Scrolling

Here's what to know about scrolling in the right pane:

* You should only be able to scroll vertically.
* You can only see the content you've scrolled to (nothing above or below).
* The scrollbar is part of the webview content.

:::image type="content" source="../assets/images/calls-and-meetings/right-pane-scroll.png" alt-text="Illustration showing how scrolling the webview content in the right pane works." border="false":::

### Navigation

For scenarios with navigation layers or heavy content, we recommend allowing users to navigate to a secondary layer. Users must be able to go back to the previous layer.

:::image type="content" source="../assets/images/calls-and-meetings/right-pane-nav.png" alt-text="Illustration showing how navigating to a secondary layer in the right pane works." border="false":::

## Components

Right panes are built primarily with the following UI components (which are based on the [Fluent UI Design System](https://fluentsite.z22.web.core.windows.net/)).

Component | Guidelines | Example
 - | - | -
[Button](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10089) | Primary and secondary buttons can be medium or small | Send a response
[Input](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10102) | Field for brief user input. Label text can include an icon  | Enter feedback
[Dropdown](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10115) | Select one or more options from a list. Can include search and multi-selection features | Choose a language
[Selection controls](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10128) | Use checkboxes for multiple choices or radio buttons and toggles for single choices. For more detailed selections, use a slider | Vote in a poll
[Error banners](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10141) | Whether displaying an urgent message, error state, or warning, the message should be short and won't interrupt the user's current task | Display issue when submitting a response

## Theming

### Colors

Use the [recommended color scheme](https://www.figma.com/file/cqL4AfKxnjKYjcv5jbgfMv/Principles-and-guidelines?node-id=280%3A3102) for backgrounds, foregrounds, and conveying states in meeting notification modals.

[See the full color scheme](https://www.figma.com/file/cqL4AfKxnjKYjcv5jbgfMv/Principles-and-guidelines?node-id=257%3A15339)

### Typography

Use the [recommended font sizes and weights](https://www.figma.com/file/cqL4AfKxnjKYjcv5jbgfMv/Principles-and-guidelines?node-id=258%3A16040) for titles, body text, and metadata text.

## Best practices

### Responsiveness

Remember, the right pane is a tab. Layouts should be able to scale to various sizes. Consider how the tab will scale and take shape before, during, and after the meeting.

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/right-pane-before-meeting.png" alt-text="Illustration showing that the right pane content looks like a full-screen tab before a meeting." border="false":::

#### Before the meeting

Make sure your tab layout can adapt to a right to left layout for different languages and that controls move to the right locations.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/right-pane-during-meeting.png" alt-text="Illustration showing how the pre-meeting tab content is condensed to the right pane during a meeting." border="false":::

#### During the meeting

Tab content moves to the right pane.

   :::column-end:::
:::row-end:::

### Theming

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/right-pane-theming-do.png" alt-text="Illustration showing how you should design the right pane for the dark theme used in Teams meetings." border="false":::

#### Do: Design for a dark theme

Teams meetings are optimized for dark mode to help reduce visual and cognitive noise so users can focus on the discussion and shared content.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/right-pane-theming-dont.png" alt-text="Illustration showing you shouldn't use colors that aren't conducive to the Teams dark theme." border="false":::

#### Don't: Use unfamiliar colors

Colors that clash with the meeting environment may be distracting and appear less native to Teams.

   :::column-end:::
:::row-end:::

### Scrolling

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/right-pane-scroll-do.png" alt-text="Illustration showing you should only allow vertical scrolling in the right pane." border="false":::

#### Do: Scroll vertically

Users anticipate vertical scrolling in Teams (and elsewhere).

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/right-pane-scroll-dont.png" alt-text="Illustration showing showing you shouldn't allow horizontal scrolling in the right pane." border="false":::

#### Don't: Scroll horizontally

Horizontal scrolling isn’t an expected behavior in Teams. Other panes in the meeting environment scroll vertically.

   :::column-end:::
:::row-end:::

### Layout

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/right-pane-layout-do.png" alt-text="Illustration showing the recommended single-column layout in the right pane." border="false":::

#### Do: Single columns

Given the right pane’s narrow nature, we strongly recommend displaying the contents in a single column.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/right-pane-layout-dont.png" alt-text="Illustration showing how a two-column layout in the right pane isn't ideal." border="false":::

#### Don't: Multiple columns

Due to the limited space of the right pane, layouts with more than one column aren’t recommended.

   :::column-end:::
:::row-end:::

### Navigation

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/right-pane-nav-do.png" alt-text="Illustration showing you should always provide a back button if your right pane app has more than one layer of navigation." border="false":::

#### Do: Have a back button

If you have more than one layer of navigation, users must be able to go back to their previous view.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/right-pane-nav-dont.png" alt-text="Illustration showing that adding another close button in the right pane for navigation is redundant and could cause issues." border="false":::

#### Don't: Include another close button

Providing an option to close right pane content may cause issues since there’s already a close button in the header to dismiss the right pane itself.

   :::column-end:::
:::row-end:::

:::row:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/right-pane-nav-caution.png" alt-text="Illustration showing that you need to be cautious when using modals (i.e., task modules) in the right pane given the limited space." border="false":::

#### Caution: Using modals in a narrow space

Modals (known as task modules in Teams) in the already narrow right pane might wrap the content and obscure the information.

   :::column-end:::
:::row-end:::

## Mobile

Some text (may remove)

## Sample app

Partner showcase and templates.

## Resources

* [Meeting extensions Figma file](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=254%3A35598)

## Validate your design

If you plan to publish your app to AppSource, you should understand what design issues commonly cause apps to fail during submission.

> [!div class="nextstepaction"]
> [Check design validation guidelines](https://review.docs.microsoft.com/en-us/microsoftteams/platform/concepts/deploy-and-publish/appsource/prepare/frequently-failed-cases?branch=restructure-design-topics-ia#validation-guidelines)
