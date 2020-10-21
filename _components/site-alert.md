---
permalink: /components/alert/
redirect_from:
- /site-alert/
- /components/site-alert/
layout: styleguide
type: component
title: Site Alert
category: Components
lead: A site alert contains critical, timely warnings or directions that have greater urgency or higher priority than content typically found on a site.
---

{% include code/preview.html component="site-alert" %}
<section class="site-component-section">
  {% include code/accordion.html component="site-alert" %}
  <div class="usa-accordion usa-accordion--bordered site-accordion-docs">
    <button class="usa-button-unstyled usa-accordion__button"
        aria-expanded="true" aria-controls="alert-docs">
      Guidance
    </button>
    <div id="alert-docs" aria-hidden="false" class="usa-accordion__content site-component-usage">
      <h4>When to use the site alert component</h4>
      <ul class="usa-content-list">
        <li><strong>System status messages.</strong> As a notification that keeps people informed of the status of the system and which may or may not require the user to respond. This includes errors, warnings, and general updates.</li>
        <li><strong>Validation messages.</strong> As a validation message that alerts someone that they just did something that needs to be corrected or as confirmation that a task was completed successfully.</li>
      </ul>
      <h4>When to consider something else</h4>
      <ul class="usa-content-list">
        <li><strong>Responding to actions taken by a user.</strong> The Alert component is useful for validation messages or informing a user that a task was completed successfully.</li>
        <li><strong>Long forms.</strong> On long forms, always include in-line validation in addition to any error messages that appear at the top of the form. </li>
        <li><strong>Destructive actions.</strong> If an action will result in destroying a user’s work (for example, deleting an application) use a more intrusive pattern, such as a confirmation modal dialogue, to allow the user to confirm that this is what they want.</li>
      </ul>
      <h4>Usability guidance</h4>
      <ul class="usa-content-list">
        <li><strong>Avoid stacking multiple emergency alert banners.</strong> Use the "Grid contained with list" variant to provide a list of links to multiple, simultaneous emergency alerts.</li>
        <li><strong>Consider the psychological impact of color.</strong> It may be tempting to make heavy use of red or orange to draw attention to the emergency alert banner. Such colors, however, can produce emotional reactions such as fear. Positioning the banner at the top of the screen provides dominance so use of bold colors may not be necessary.</li>
        <li><strong>Consider next steps.</strong> When the user is required to do something in response to an alert, let them know what they need to do and make that task as easy as possible. Think about how much context to provide with your message. For example, a notification of a system change may require more contextual information than a validation message. Write the message in concise, human readable language; avoid jargon and computer code.</li>
        <li><strong>Be polite.</strong> Be polite in error messages — don’t blame the user.</li>
        <li><strong>Alerts are an opportunity.</strong> Users will read a message that helps them resolve an error even if they generally won’t read documentation; include some educational material in your error message.</li>
        <li><strong>Don’t overdo it.</strong> Too many notifications will either overwhelm or annoy the user and are likely to be ignored.</li>
        <li><strong>Allow a user to dismiss a notification wherever appropriate.</strong></li>
        <li><strong>Understand the user’s context.</strong> Don’t include notifications that aren’t related to the user’s current goal.</li>
      </ul>
      <h4>Accessibility</h4>
      <ul class="usa-content-list">
        <li><strong>Use the proper ARIA role.</strong> If the message is not interactive, use the ARIA <code>role=<wbr>"alert"</code> to inform assistive technologies of a time-sensitive and important message. If the message is interactive, use the use the ARIA <code>role=<wbr>"alertdialog"</code> instead.</li>
        <li><strong>Don’t visually hide alert messages and then make them visible when they are needed.</strong> Users of older assistive technologies may still be able to perceive the alert messages even if they are not currently applicable.</li>
      </ul>
      <h4 class="usa-heading">Implementation</h4>
      <h5 id="component-settings">Alert settings</h5>
      {% assign settings = site.data.settings.components.alert %}
      {% include settings-table-simple.html
        settings=settings.contents
      %}
      <h5 id="component-variants">Alert variants</h5>
      <table class="usa-table--borderless site-table-responsive site-table-simple" aria-labelledby="component-variants">
        <thead>
          <tr>
            <th scope="col" class="flex-6">Variant</th>
            <th scope="col" class="flex-6">Description</th>
          </tr>
        </thead>
        <tbody class="font-mono-2xs">
          <tr>
            <td data-title="Variant" class="flex-6">usa-site-alert--info</td>
            <td data-title="Description" class="flex-6">
              <span class="font-lang-3xs">Display an informational status site alert.</span>
            </td>
          </tr>
          <tr>
            <td data-title="Variant" class="flex-6">usa-site-alert--warning</td>
            <td data-title="Description" class="flex-6">
              <span class="font-lang-3xs">Display a warning status site alert.</span>
            </td>
          </tr>
          <tr>
            <td data-title="Variant" class="flex-6">usa-site-alert--emergency</td>
            <td data-title="Description" class="flex-6">
              <span class="font-lang-3xs">Display an emergency status site alert.</span>
            </td>
          </tr>
          <tr>
            <td data-title="Variant" class="flex-6">usa-site-alert--error</td>
            <td data-title="Description" class="flex-6">
              <span class="font-lang-3xs">Display an error status site alert.</span>
            </td>
          </tr>
          <tr>
            <td data-title="Variant" class="flex-6">usa-site-alert--success</td>
            <td data-title="Description" class="flex-6">
              <span class="font-lang-3xs">Display a success status site alert.</span>
            </td>
          </tr>
          <tr>
            <td data-title="Variant" class="flex-6">usa-site-alert--slim</td>
            <td data-title="Description" class="flex-6">
              <span class="font-lang-3xs">Display a slimmer version of the site alert.</span>
            </td>
          </tr>
          <tr>
            <td data-title="Variant" class="flex-6">usa-site-alert--no-icon</td>
            <td data-title="Description" class="flex-6">
              <span class="font-lang-3xs">Display an site alert without an icon.</span>
            </td>
          </tr>
        </tbody>
      </table>
      <h4 class="usa-heading">Package information</h4>
      <ul class="usa-content-list">
        <li>
          <strong>Package usage:</strong> <code>@import usa-alert</code>
        </li>
        <li>
          <strong>Requires:</strong> <code>required</code>, <code>global</code>
        </li>
      </ul>
    </div>
  </div>
</section>
