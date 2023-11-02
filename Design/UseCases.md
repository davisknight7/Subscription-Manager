## Actors

1. **Advisor**
    - Primary users of the system. They can view and manage their own Moneytree subscriptions, update personal details,
      and interact with the platform's core features.

2. **Account Manager**
    - Moneytree employee who enters the details of advisors during bulk sign-up.

3. **System**
    - Represents automated processes and integrations, such as updating subscription statuses in Maxio or synchronizing
      data with HubSpot.

4. **Maxio**
    - The external subscription management system with which the platform integrates for subscription data.

5. **HubSpot**
    - Another external system for customer relationship management. The platform sends updated user data to HubSpot.

## Use Cases

- **UC1**: **View Subscription Details**
    - **Reason**: Users need to view details of their subscriptions. This ensures users are informed about the specifics
      of their services.
    - **Actors**: Advisor
    - **Flow**:
        1. Advisor logs into the system.
        2. Advisor navigates to the subscription management page.
        3. System retrieves and displays the Advisor's subscription details.
    - **Connected Business Requirement**: Unified Subscription View
- **UC2**: **User Wants To View Their Next Payment Date**
    - **Reason**: To keep users informed on when payments are due the system needs to show specific information on their
      subscriptions.
    - **Actors**: Advisor
    - **Flow**:
        1. Advisor clicks on one of their subscriptions on the subscription management page.
        2. They navigate to an individual subscription page.
        3. The system retrieves and displays the next payment date for the subscription.
    - **Connected Business Requirement**: Unified Subscription View
- **UC3**: **Bulk Sign-Up 12 of Advisors**
    - **Reason**: As the platform aims to cater to larger organizations and groups of advisors, a bulk sign-up feature
      is essential. This eliminates the inefficiencies of one-by-one registrations, catering to the scalability needs of
      Moneytree.
    - **Actors**: Account Manager
    - **Flow**:
        1. Account manager navigates to the bulk sign-up page.
        2. Account manager enters details of the first advisor.
        3. Account manager uses the interface to dynamically add 11 more advisors.
        4. Account manager submits the form.
        5. System processes the data and registers the advisors in maxio and hubspot.
    - **Connected Business Requirement**: Bulk Sign Up
- **UC4**: **Bulk Sign-Up with Additional Services**
    - **Reason**: Organizations might select different products for their advisors.
    - **Actors**: Account Manager
    - **Flow**:
        1. Account manager navigates to the bulk sign-up page.
        2. Account manager enters details of the first advisor.
        3. Account manager selects the desired core product for the first advisor.
        4. Account manager selects optional additional products for the first advisor.
        5. Repeat steps 2-4 for each advisor.
    - **Connected Business Requirement**: Bulk Sign Up
- **UC5**: **Modify Subscription Details**
    - **Reason**: Users may need to adjust their subscription details based on changing requirements or preferences.
      Providing them with the capability to modify their subscriptions ensures flexibility.
    - **Actors**: Advisor
    - **Flow**:
        1. Advisor logs into the system.
        2. Advisor navigates to the subscription modification page.
        3. Advisor makes desired changes.
        4. System updates the subscription data and reflects the changes in Maxio.
    - **Connected Business Requirement**: Subscription Modification
- **UC6**: **Add Additional Product**
    - **Reason**: Users may want to add additional products to their subscription.
    - **Actors**: Advisor
    - **Flow**:
        1. Advisor clicks add additional product button on the subscription modification page.
        2. Advisor selects the desired additional product.
        3. System validates that the selected subscription is allowed for their core product.
        4. System updates their total subscription payment.
        5. System updates the subscription data and reflects the changes in Maxio.
    - **Connected Business Requirement**: Subscription Modification

