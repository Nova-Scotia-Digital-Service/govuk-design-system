---
title: Summary list
description: Use the summary list to summarise information, for example, a user’s responses at the end of a form.
section: Components
aliases:
backlog_issue_id: 182
layout: layout-pane.njk
---

{% from "_example.njk" import example %}

Use the summary list to summarise information, for example, a user’s responses at the end of a form.

{{ example({group: "components", item: "summary-list", example: "default", html: true, nunjucks: true, open: false}) }}

## When to use this component

Use the summary list component to present pairs of related information, known as key-value pairs, in a list. The key is a description or label of a piece of information, like ‘Name’, and the value is the piece of information itself, like ‘John Smith’.

You can use it to display metadata like ‘Last updated’ with a date like ‘22 June 2018’, or to summarise a user’s responses at the end of a form like the [check answers](/patterns/check-answers/) pattern.

## When not to use this component

The summary list uses the description list (`<dl>`) HTML element, so only use it to present information that has a key and at least one value.

Do not use it for tabular data or a simple list of information or tasks, like a [task list](/patterns/task-list-pages/). For those use a `<table>`, `<ul>` or `<ol>`.


## How it works

There are 2 ways to use the summary list component. You can use HTML or, if you’re using [Nunjucks](https://mozilla.github.io/nunjucks/) or the [GOV.UK Prototype Kit](https://prototype-kit.service.gov.uk), you can use the Nunjucks macro.

{{ example({group: "components", item: "summary-list", example: "without-actions", html: true, nunjucks: true, open: false}) }}

###  Adding actions to each row

You can add actions to a summary list, like a ‘Change’ link to let users go back and edit their answer.

For sighted users, the actions get their context from the other content in the row they appear in.

Assistive technology users, like those who use a screen reader, may hear the links out of context and not know what they do.

To give more context, add visually hidden text to the links. This means a screen reader user will hear a meaningful action, like ‘Change name’ or ‘Change date of birth’.

{{ example({group: "components", item: "summary-list", example: "default", html: true, nunjucks: true, open: false, titleSuffix: "second"}) }}

If you have a mix of rows with and without actions, add the `govuk-summary-list__row--no-actions` modifier class to the rows without actions.

{{ example({group: "components", item: "summary-list", example: "mixed-actions", html: true, nunjucks: true, open: false}) }}

### Removing the borders

The summary list includes some separating borders to help users read each row and its action.

If your summary list does not have any actions, you can choose to remove the separating borders with the `govuk-summary-list--no-border` class.

{{ example({group: "components", item: "summary-list", example: "without-borders", html: true, nunjucks: true, open: false}) }}

To remove borders on a single row, use the `govuk-summary-list__row--no-border` class.

## Research on this component

This component was developed and tested by the Government Digital Services as part of the [check answers pattern](/patterns/check-answers/).

### Next steps

More research is needed to find out how well this component works outside the check answers pattern, for example, to present summaries within caseworking systems.

If you use this component in your service, get in touch to share your research findings.
