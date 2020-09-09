---
title: Designing the Microsoft Teams meeting right pane
author: heath-hamilton
description: Guidance and best practices for designing the meeting right pane for Microsoft Teams.
ms.author: heath-hamilton
ms.topic: conceptual
---
# Designing the meeting right pane

The right pane is a canvas for augmenting collaboration during meetings. Attendees can see and interact with app content in a dedicated space outside the meeting stage through shared or role-based views.

## Use cases

People might use the right pane during meetings to:

* Submit detailed feedback (for example, evaluate a job candidate)
* Quickly create a poll, survey, or task item for the meeting participants
* Display notes relevant to the meeting (for example, information about a sales lead)

## Example

The following example shows the right pane displaying survey app content during a meeting.

:::image type="content" source="../assets/images/calls-and-meetings/right pane-organizer-view.png" alt-text="Example shows what the meeting right pane might look like from a meeting organizer's perspective.":::

[See the full scenario](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=208%3A9816)

[See other example use cases](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=218%3A10461)

## Anatomy

The right pane essentially is a Teams tab that displays content with the following dimensions:

* **Width**: 280 pixels (with 20 pixels of padding on either side)
* **Height**: Full bleed to the bottom of the right pane. There are 20 pixels of padding between the right pane header and the webview.

:::image type="content" source="../assets/images/calls-and-meetings/right-pane-anatomy.png" alt-text="Illustration showing the UI anatomy of a meeting extension right pane." border="false":::

1. **App icon**: The entry point to the right pane.
1. **Right pane header**: Includes tab name, more actions, and close.
1. **Tab name**: The name of the tab instance.
1. **More actions**: Provides options on hover that include:
   * Reload the tab.
   * Rename the tab.
   * Mute notifications from the app during the meeting.
   * Open app settings and About modal.
   * Remove the tab from the meeting.
1. **Dismiss**: Dismisses the right pane. Always use the upper-right close icon instead of an acton in the footer.
1. **Webview**: Displays all third-party content.

## Behavior

Some text and art.

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

These Teams-specific guidelines can help you quickly and confidently choose the right colors and typography.

### Colors

Use the [recommended color scheme](https://www.figma.com/file/cqL4AfKxnjKYjcv5jbgfMv/Principles-and-guidelines?node-id=280%3A3102) for backgrounds, foregrounds, and conveying states in meeting notification modals.

[See the full color scheme](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=257%3A15339)

### Typography

Use the [recommended font sizes and weights](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=257%3A15511) for titles, body text, and metadata text.

## Best practices

Some text

### Theming

:::row:::
   :::column span="":::
:::image type="content" source="image" alt-text="Illustration showing ... ." border="false":::

#### Do: Some text

Some text

   :::column-end:::
   :::column span="":::
:::image type="content" source="image" alt-text="Illustration showing ... ." border="false":::

#### Don't: Some text

Some text

   :::column-end:::
:::row-end:::

### Scrolling

:::row:::
   :::column span="":::
:::image type="content" source="image" alt-text="Illustration showing ... ." border="false":::

#### Do: Some text

Some text

   :::column-end:::
   :::column span="":::
:::image type="content" source="image" alt-text="Illustration showing ... ." border="false":::

#### Don't: Some text

Some text

   :::column-end:::
:::row-end:::

### Layout

:::row:::
   :::column span="":::
:::image type="content" source="image" alt-text="Illustration showing ... ." border="false":::

#### Do: Some text

Some text

   :::column-end:::
   :::column span="":::
:::image type="content" source="image" alt-text="Illustration showing ... ." border="false":::

#### Don't: Some text

Some text

   :::column-end:::
:::row-end:::

### Navigation

:::row:::
   :::column span="":::
:::image type="content" source="image" alt-text="Illustration showing ... ." border="false":::

#### Do: Some text

Some text

   :::column-end:::
   :::column span="":::
:::image type="content" source="image" alt-text="Illustration showing ... ." border="false":::

#### Don't: Some text

Some text

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
