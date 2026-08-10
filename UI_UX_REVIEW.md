# UI/UX review notes

This review records the interaction decisions behind the paired-photo webapp.
It is a product-quality review, not a claim of clinical usability validation.

## Reference patterns

- [CMS Design System forms](https://design.cms.gov/patterns/Forms/forms/?theme=healthcare): keep forms simple, keep visual and document order aligned, and provide enough spacing between fields.
- [CMS Design System buttons](https://design.cms.gov/components/button/): use consistent button styles and clear action language.
- [Primer buttons](https://primer.style/product/components/button/): use one primary action sparingly, pair it with secondary actions, and treat destructive actions as distinct.
- [GOV.UK button guidance](https://design-system.service.gov.uk/components/button/): group related buttons and keep button behavior explicit.
- [Carbon button guidance](https://preview.carbondesignsystem.com/building-blocks/core/components/button/guidelines): reserve the primary button for the principal action and provide an explicit in-progress state when work takes time.

## Applied decisions

- The capture section now presents `Load demo pair` as a visible secondary action instead of a low-contrast text link.
- The automatic first pass appears before manual scale fields because it is the intended low-effort route.
- Advanced settings occupy a full row rather than leaving an empty half-column beside a disclosure.
- `Review the change` explains its prerequisite while disabled: `Add both photos to continue`.
- The destructive `Clear` action is disabled until local history exists.
- The primary action remains singular for each workflow stage; report download and reset remain secondary/text actions.
- Clinical limitations stay visible near the top and at the result, rather than being hidden behind a help panel.

## Remaining validation

The interface still needs moderated usability testing with representative clinical-research users, keyboard-only testing on supported browsers, and device testing at 320px, 768px, and desktop widths. These are human-factors checks, not substitutes for clinical validation.
