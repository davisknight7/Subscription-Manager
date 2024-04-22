# For Future

## Known Issues
### Bulk Signup
- "Enter" button shortcut on advisor modal has some weird behavior. It will initially save a new advisor in the store, but when editing, "enter" does not update the store. It only updates the textbox values.
- When closing the advisor dropdown, the animation is slightly delayed. Only on closing.

### Dashboards
- Sometimes, 'npm run build --ws' will fail depending on the computer/environment which it is run on.
- Subscription Group tab still shows if the customer is not part of a subscription group.
- Advise dashboard shows 'not found' due to incorrect product handle in testing environement.
- Chart not displaying correctly on initial load.

### Onboarding
- Submit button is not hooked up to any endpoint.

## Known Improvements
### Bulk Signup
- Potentially, could add support for multiple products. AdvisorModal.vue and ProductSelection.vue are the relevant files for this. AdvisorModalValidator would also need updated.
- Validation does not clear when closing and reopening the add advsior modal
- Could add more shortcuts for stepping, escaping, deleting, etc.

### Dashboards
- Inside backend method FindSubscriptionGroup, the error caught, but just thrown and logged as 404. Could be handled better. Could have better error handling in general.
- Maxio SDK could significantly improve development and less tech debt.
- The configs are duplicated across all apps, but they probably should be shared. Could create shared configs packages including customer and product config. Customer config is only for development.
- Add searching and filters to invoice table
- Clicking anywhere in invoice table row opens modal, rather than a single link on invoice number
- Only Subscription Overview component changes color based on product prop. This is a start example on changing styles based on product dashboard. It is not done anywhere else besides this component.
- There could be better error displaying. Currently it is just some red text on a white background in the dashboard when the product fails. Could be changed to display nicer. Individual api calls failing could result . ErrorDisplay is the component for the fallback error. In AsyncDataRenderer you can pass an optional error componet and a required fallback component. Currently fallback is spinner. There are some places where an ErrorDisplay component which results in an infinite spinner. That can be improved/fixed by passing ErrorDisplay components as props to AsyncDataRenderer components that do not have it.
- Switch to Vite env variables for getting the mode that the app is in for products config. See this article: https://vitejs.dev/guide/env-and-mode#modes
- appsettings.json has the api key and cors allowed hosts. It is currently set to "*".
- Backend models could have a more organized naming scheme and folder strucutre.

### Onboarding
- Backend does not have a customer creation endpoint.
- Validation on steps does not reset when flipping through steps. Potential change depending on how that should work.
