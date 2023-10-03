## Actors

1. **Advisor**
    - Primary users of the system. They can view and manage their own Moneytree subscriptions, update personal details, and interact with the platform's core features.

2. **Account Manager**
    - Responsible for managing the subscriptions of multiple advisors, especially during bulk sign-ups. They have access to more administrative features and can handle larger-scale operations.

3. **System**
    - Represents automated processes and integrations, such as updating subscription statuses in Maxio or synchronizing data with HubSpot.

4. **Maxio**
    - The external subscription management system with which the platform integrates for subscription data.

5. **HubSpot**
    - Another external system for customer relationship management. The platform sends updated user data to HubSpot.

## Use Cases

- **UC1**: **View Subscription Details**
    - **Reason**: Users need to view details of their subscriptions. This ensures users are informed about the specifics of their services.
    - **Actors**: Advisor
    - **Flow**:
        1. Advisor logs into the system.
        2. Advisor navigates to the subscription management page.
        3. System retrieves and displays the Advisor's subscription details.
    - **Connected Business Requirement**: Unified Subscription View

- **UC2**: **Bulk Sign-Up of Advisors**
    - **Reason**: As the platform aims to cater to larger organizations and groups of advisors, a bulk sign-up feature is essential. This eliminates the inefficiencies of one-by-one registrations, catering to the scalability needs of Moneytree.
    - **Actors**: Account Manager
    - **Flow**:
        1. Account manager navigates to the bulk sign-up page.
        2. Account manager enters details of the first advisor.
        3. Account manager uses the interface to dynamically add more advisors.
        4. Account manager submits the form.
        5. System processes the data and registers the advisors.
    - **Connected Business Requirement**: Bulk Sign Up

- **UC3**: **Modify Subscription Details**
    - **Reason**: Users may need to adjust their subscription details based on changing requirements or preferences. Providing them with the capability to modify their subscriptions ensures flexibility.
    - **Actors**: Advisor
    - **Flow**:
        1. Advisor logs into the system.
        2. Advisor navigates to the subscription modification page.
        3. Advisor makes desired changes.
        4. System updates the subscription data and reflects the changes in Maxio.
    - **Connected Business Requirement**: Subscription Modification

