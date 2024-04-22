#For Future

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
- Potentially, could add support for multiple products

### Dashboards
- Inside backend method FindSubscriptionGroup, the error caught, but just thrown and logged as 404. Could be handled better. Could have better error handling in general.
- Maxio SDK could significantly improve development and less tech debt.
- The configs are duplicated across all apps, but they probably should be shared. Could create shared configs packages including customer and product config. Customer config is only for development.
- Add searching and filters to invoice table
- Clicking anywhere in invoice table row opens modal, rather than a single link on invoice number
- 

### Onboarding
- Backend does not have a customer creation endpoint.
- Validation on steps does not reset when flipping through steps. Potential change depending on how that should work.
