---
title: Designing a Microsoft Teams in-meeting dialog
author: heath-hamilton
description: Guidance and best practices for designing an in-meeting dialog for Microsoft Teams.
ms.author: lajanuar
ms.topic: conceptual
---
# Designing an in-meeting dialog

In-meeting dialogs display on the Teams meeting stage. They require a user's attention, confirmation, or interaction but are subtle and don't interrupt the meeting.

## Use cases

In-meeting dialogs are triggered by a user. You might create one of these dialogs so users can:

* Provide brief feedback
* Take a short survey or poll
* Submit approvals
* Get reminders

## Example

The following example shows what the in-meeting dialog might look like from a meeting participant's perspective. As you can see, the content and task are lightweight.

:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-participant-view.png" alt-text="Example shows what the in-meeting dialog might look like from a meeting participant's perspective.":::

<a href="https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=208%3A9816" target="_blank">See the full scenario (Figma)</a>

<a href="https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=2292%3A14353" target="_blank">See other example use cases (Figma)</a>

## Anatomy

:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-anatomy.png" alt-text="Illustration showing the UI anatomy of an in-meeting dialog." border="false":::

In-meeting dialogs are comprised of the following parts:

1. **App icon**
1. **App name**
1. **Action string**
1. **Dismiss icon:** Closes a single notification. Always use the upper-right close icon instead of an action in the footer.
1. **Webview**: Displays all third-party app content and buttons (standard Teams buttons recommended).

### Sizing

In-meeting dialogs can vary in size to account for different scenarios. Make sure to maintain padding and component sizes.

* **Height**: The height of the dialog is determined by the content in the webview. Vertical scroll takes over for content that exceeds the maximum height (defined by you).
* **Width**: The width of the webview is an absolute value within the range you specify.

:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-sizing.png" alt-text="Illustration showing the UI anatomy of an in-meeting dialog." border="false":::

## Behavior

See general in-meeting dialog behavior, such as rest, loading, and more, in [Figma](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=2292%3A17985).

### Position

In-meeting dialogs are aligned in the center of the meeting stage. They can’t be dragged and work within the framework of Teams system-level notifications.

:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-position.png" alt-text="Illustration showing the UI anatomy of an in-meeting dialog." border="false":::

### Aggregation

Only one dialog displays at a time, stack ranking from last to most recent sent at the back. Once a dialog is resolved or dismissed, the next one take its place.

[See an example (Figma)](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=2292%3A17985)

### Scrolling

Scrolling occurs in the webview portion of an in-meeting dialog. Remember the following about scrolling:

* You should only be able to scroll vertically.
* You can only see the content you've scrolled to (nothing above or below).

:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-scroll.png" alt-text="Illustration showing how scrolling the webview content in the in-meeting dialog works." border="false":::

### Buttons

In-meeting dialog buttons are part of the webview ([see some examples](#best-practices)). 

Unlike similar components, in-meeting dialogs are dismissed once I user selects a button.

## Components

in-meeting dialogs are built primarily with the following UI components (which are based on the [Fluent Design System](https://fluentsite.z22.web.core.windows.net/)).

Component | Guidelines | Example
 - | - | -
[Button](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10089) | Primary and secondary buttons can be medium or small | Send a response
[Input](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10102) | Field for brief user input. Label text can include an icon  | Enter feedback
[Dropdown](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10115) | Select one or more options from a list. Can include search and multi-selection features | Choose a language
[Selection controls](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10128) | Use checkboxes for multiple choices or radio buttons and toggles for single choices. For more detailed selections, use a slider | Vote in a poll
[Alerts](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10141) | Whether displaying an urgent message, error state, or warning, the message should be short and won't interrupt the user's current task | Display issue when submitting a response

## Theming

### Colors

Use the [recommended color scheme](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=280%3A4030) for backgrounds, foregrounds, and conveying states in in-meeting dialogs.

[See the full color scheme](https://www.figma.com/file/cqL4AfKxnjKYjcv5jbgfMv/Principles-and-guidelines?node-id=257%3A15339)

### Typography

Use the [recommended font sizes and weights](https://www.figma.com/file/cqL4AfKxnjKYjcv5jbgfMv/Principles-and-guidelines?node-id=258%3A16040) for titles, body text, and metadata text.

## Best practices

While in-meeting dialogs can make calls more effective, they also can derail calls if too obtrusive. Allowing the organizer to share this content and participants to quickly view and interact with it is paramount to a good experience. In general, use these types of dialogs sparingly and make sure they follow these guidelines.

### Navigation

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-steps-do.png" alt-text="Illustration showing how to limit in-meeting dialog content to a single screen so users can focus on the meeting." border="false":::

#### Do: Keep it contained

Limit in-meeting dialog content to a single screen so users can focus on the meeting.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-steps-dont.png" alt-text="Illustration showing how in-meeting dialogs shouldn't require users to navigate through content." border="false":::

#### Don't: Include multiple steps

in-meeting dialogs shouldn't require users to navigate through content.

   :::column-end:::
:::row-end:::

### Interactions

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-interactions-do.png" alt-text="Illustration showing why you should remove unnecessary content that doesn't help users accomplish something quickly." border="false":::

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-interactions-dont.png" alt-text="Another illustration showing why you should remove unnecessary content that doesn't help users accomplish something quickly." border="false":::

   :::column-end:::
:::row-end:::

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-tab-do.png" alt-text="Illustration showing that, if you need complex interactions, it's recommended you use a single column on the meeting right pane instead." border="false":::

#### Do: Limit the number of possible interactions

Remove unnecessary content that doesn't help users accomplish something quickly. If you need complex interactions, we strongly recommend using a single column in the meeting tab instead.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-tab-dont.png" alt-text="Illustration showing that too many interactions in the in-meeting dialog distracts from the meeting." border="false":::

#### Don't: Introduce unnecessary elements

You may be able to design a single in-meeting dialog with multiple interactions, but too many can distract from the meeting.

   :::column-end:::
:::row-end:::

### Layout

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-layout-do.png" alt-text="Illustration showing an ideal layout for in-meeting dialogs." border="false":::

#### Do: Use single-column layouts

Since the dialogs are at the center of the meeting stage, task completion should be fast and simple to avoid user frustration.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-layout-dont.png" alt-text="Illustration showing layout for in-meeting dialogs that isn't recommended." border="false":::

#### Don't: Clutter the space

Dense content can be distracting and overwhelming, especially during a meeting.

   :::column-end:::
:::row-end:::

### Size

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-size-do.png" alt-text="Illustration showing how the in-meeting dialog size should always be the same." border="false":::

#### Do: Keep it consistent

This is important because in-meeting dialogs always display in the same location.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-size-dont.png" alt-text="Illustration showing how you shouldn't use different dialog sizes." border="false":::

#### Don't: Always fit to the content

You may be trying to avoid horizontal scrolling, but multiple in-meeting dialog sizes within the same app is an inconsistent experience.

   :::column-end:::
:::row-end:::

### Controls

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-controls-do.png" alt-text="Illustration showing where to place buttons on the in-meeting dialog." border="false":::

#### Do: Right align the primary action

We recommend positioning the most visually heavy action to the right-most location.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/in-meeting-dialog-controls-dont.png" alt-text="Illustration showing where not to place buttons on the in-meeting dialog." border="false":::

#### Don't: Left or center align actions

Doing so deviates from the standard Teams pattern for control placement in a dialog and may conflict with a dialog behind the top one.

   :::column-end:::
:::row-end:::

## Accessibility

For information on accessibility, see [Figma](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=2292%3A15397).

## Resources

* [Meeting extensions Figma file](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=254%3A35598)

## Validate your design

If you plan to publish your app to AppSource, you should understand what design issues commonly cause apps to fail during submission.

> [!div class="nextstepaction"]
> [Check design validation guidelines](https://review.docs.microsoft.com/en-us/microsoftteams/platform/concepts/deploy-and-publish/appsource/prepare/frequently-failed-cases?branch=restructure-design-topics-ia#validation-guidelines)
