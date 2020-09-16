---
title: Designing a Microsoft Teams in-meeting dialog
author: heath-hamilton
description: Guidance and best practices for designing an in-meeting dialog for Microsoft Teams.
ms.author: lajanuar
ms.topic: conceptual
---
# Designing an in-meeting dialog

In-meeting dialogs display on the Teams meeting stage. They require a user's attention, confirmation, or interaction in a way that's subtle and doesn't interrupt the meeting.

## Use cases

You might create an in-meeting dialog so users can:

* Provide brief feedback
* Take a short survey or poll
* Submit approvals
* Get reminders

## Example

The following example shows what the in-meeting dialog might look like from a meeting participant's perspective. As you can see, the content and task are lightweight.

:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-participant-view.png" alt-text="Example shows what the in-meeting dialog might look like from a meeting participant's perspective.":::

<a href="https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=208%3A9816" target="_blank">See the full scenario (Figma)</a>

<a href="https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=218%3A10461" target="_blank">See other example use cases (Figma)</a>

## Anatomy

In-meeting dialogs are responsive and have the following dimensions:

* **Width**: Minimum 280 pixels and maximum 460 pixels
* **Height**: Auto height with a maximum 400 pixels (300 for the content area)

:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-anatomy.png" alt-text="Illustration showing the UI anatomy of an in-meeting dialog." border="false":::

1. **Avatar**: User who initiated the dialog.
1. **App attribution**: App icon and name.
1. **Action string**: Describes what the user who initiated the dialog wants to do: [*User*][*action*].
1. **More actions**: Provides options on hover that include:
   * Mute notifications from the app during the meeting.
   * Dismiss all notifications on the screen.
   * Manage notification settings.
   * Use an action-based messaging extension.
   * Expand the notification on the meeting stage.
1. **Dismiss**: Dismisses a single notification. Always use the upper-right close icon instead of an action in the footer.
1. **Actions**: Optional (depends on your use case).
1. **Input error**: When required, displays a short error message.
1. **Aggregate count**: When required, shows if there's more than one active dialog (count includes all apps).
1. **Webview**: Displays all third-party app content. See [webview dimensions](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=218%3A8829).

## Behavior

Here's what to know if your in-meeting dialog requires scrolling:

* You should only be able to scroll vertically.
* You can only see the content you've scrolled to (nothing above or below).
* The scrollbar is part of the webview content.

:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-scroll.png" alt-text="Illustration showing how scrolling the webview content in the in-meeting dialog works." border="false":::

## Components

in-meeting dialogs are built primarily with the following UI components (which are based on the [Fluent Design System](https://fluentsite.z22.web.core.windows.net/)).

Component | Guidelines | Example
 - | - | -
[Button](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10089) | Primary and secondary buttons can be medium or small | Send a response
[Input](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10102) | Field for brief user input. Label text can include an icon  | Enter feedback
[Dropdown](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10115) | Select one or more options from a list. Can include search and multi-selection features | Choose a language
[Selection controls](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10128) | Use checkboxes for multiple choices or radio buttons and toggles for single choices. For more detailed selections, use a slider | Vote in a poll
[Error banners](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=214%3A10141) | Whether displaying an urgent message, error state, or warning, the message should be short and won't interrupt the user's current task | Display issue when submitting a response

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
:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-steps-do.png" alt-text="Illustration showing how to limit in-meeting dialog content to a single screen so users can focus on the meeting." border="false":::

#### Do: Keep it contained

Limit in-meeting dialog content to a single screen so users can focus on the meeting.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-steps-dont.png" alt-text="Illustration showing how in-meeting dialogs shouldn't require users to navigate through content." border="false":::

#### Don't: Include multiple steps

in-meeting dialogs shouldn't require users to navigate through content.

   :::column-end:::
:::row-end:::

### Interactions

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-interactions-do.png" alt-text="Illustration showing why you should remove unnecessary content that doesn't help users accomplish something quickly." border="false":::

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-interactions-dont.png" alt-text="Another illustration showing why you should remove unnecessary content that doesn't help users accomplish something quickly." border="false":::

   :::column-end:::
:::row-end:::

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-right-pane-do.png" alt-text="Illustration showing that, if you need complex interactions, it's recommended you use a single column on the meeting right pane instead." border="false":::

#### Do: Limit the number of possible interactions

Remove unnecessary content that doesn't help users accomplish something quickly. If you need complex interactions, we strongly recommend using a single column in the meeting tab instead.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-right-pane-dont.png" alt-text="Illustration showing that too many interactions in the in-meeting dialog distracts from the meeting." border="false":::

#### Don't: Introduce unnecessary elements

You may be able to design a single in-meeting dialog with multiple interactions, but too many can distract from the meeting.

   :::column-end:::
:::row-end:::

### Layout

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-layout-do.png" alt-text="Illustration showing an ideal layout for in-meeting dialogs." border="false":::

#### Do: Use single-column layouts

Since the dialogs are at the center of the meeting stage, task completion should be fast and simple to avoid user frustration.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-layout-dont.png" alt-text="Illustration showing layout for in-meeting dialogs that isn't recommended." border="false":::

#### Don't: Clutter the space

Dense content can be distracting and overwhelming, especially during a meeting.

   :::column-end:::
:::row-end:::

### Size

:::row:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-size-do.png" alt-text="Illustration showing how the in-meeting dialog size should always be the same." border="false":::

#### Do: Keep it consistent

This is important because in-meeting dialogs always display in the same location.

   :::column-end:::
   :::column span="":::
:::image type="content" source="../assets/images/calls-and-meetings/notification-modal-size-dont.png" alt-text="Illustration showing how you shouldn't use different dialog sizes." border="false":::

#### Don't: Always fit to the content

You may be trying to avoid horizontal scrolling, but multiple in-meeting dialog sizes within the same app is an inconsistent experience.

   :::column-end:::
:::row-end:::

## Sample app

Link to sample Contoso app.

## Resources

* [Meeting extensions Figma file](https://www.figma.com/file/QjjWsZYpNqwjRc3OXTgBpp/Principles-and-guidelines?node-id=254%3A35598)

## Validate your design

If you plan to publish your app to AppSource, you should understand what design issues commonly cause apps to fail during submission.

> [!div class="nextstepaction"]
> [Check design validation guidelines](https://review.docs.microsoft.com/en-us/microsoftteams/platform/concepts/deploy-and-publish/appsource/prepare/frequently-failed-cases?branch=restructure-design-topics-ia#validation-guidelines)
