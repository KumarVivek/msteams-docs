---
title: Designing tabs in Microsoft Teams
author: heath-hamilton
description: Guidance and best practices for designing tabs in a Microsoft Teams app.
---
# Designing tabs

Designing an effective tab for Teams is similar to designing a single-page application. The best tabs are simple, task oriented, and facilitate collaboration.

## Best practices

Use these as tab design checklists.

### Dos

* **Focus on functionality** to only your app's use cases. (Teams isn't the World Wide Web.)
* **Know your audience**. Your tab may be used by one person (personal tab) or a group (channel tab), which could influence your design.
* **Use Teams design components and patterns** so that your tab feels natural within the platform.
* **Include a default state** for your tab even if users can configure some aspects of the experience.
* **Notify users of tab activity**. For example, post cards to a channel when someone creates a ticket on the issue tracker tab.
* **Be a deep link target** from elsewhere in Teams. For example, a card may show a summary of bug data, but selecting it shows all bug details in the tab.
* **Incorporate some personality** by including colors, logos, and layouts that communicate your brand.
* **Give the tab a useful name**. While your app's name may stand out in AppSource, consider naming the tab simply based on what it can do.

### Don'ts

* **Create a full website experience** with multiple panels, layers of navigation, or lots of vertical and horizontal scrolling.
* **Complicate the sign-in process**. If you need to grant access to your tab, make sure it's a simple workflow or people won't use it.
* **Focus too much on branding**. For example, keep your logo small and unobtrusive. Place it on the top right, top left, or bottom edge of the tab.

## Layouts

Here are some common tab layouts.

### Single canvas

This is a single large area where work gets done. OneNote and Wiki follow this pattern. If your app that doesn’t separate content into smaller components this would be a good fit.

!!List or table with common design components (including Figma links)!!

### List

Lists are great for sorting and filtering large quantities of data and are great at keeping the most important things at the top. It is helpful to use sortable columns. Actions can be added to each list item under the ellipsis menu.

!!List or table with common design components (including Figma links)!!

### Column

Columns are great for workflows that move an item from one column to another to indicate a new status. Consider supporting drag and drop for those scenarios. We recommend using dialogs or inline expansion for detail views.

!!List or table with common design components (including Figma links)!!

### Grid

Grids are useful for showing elements which are highly visual. It helps to include a filter or search control at the top.

!!List or table with common design components (including Figma links)!!

## Setup experiences

For tab onboarding and auth workflows (channel tab).

Tab configuration design – have sketch files + templates

Sign in/sign out – sketch files + templates

Empty state/welcome screen – best practices + sketch files

!!List or table with common design components (including Figma links)!!

## Cards and task modules

Discuss cards and task modules within context of tabs and include links to their respective design guidelines. Could also just be links to their guidelines.

## Mobile considerations

Need info from mobile design team.

## Real-world examples

Which partners have the "best" tabs? If possible, showcase different industries (e.g., health care, edu).

Is there code open source, or do we have a template that's similar we can link to?

## Related resources

* Figma sketch files
* Card and task module design guidelines
* Developer section of tabs (how to get started building)