# Manage OTPaaS Whitelists

## Overview
This serves as a guide for managing OTP app whitelists via the TechPass portal. This allows tenants to restrict users that can use their services via OTPaaS.

## Getting Started
Make sure to have onboarded OTPaaS and created one or more OTP apps. More information about OTPaaS can be found [here](otpaas/otpaas.md).

## Viewing whitelists of OTP App
1. Make sure you have the `TENANT` role selected (on the top right on the navigation bar).

2. Go to your namespace. 
3. On the left side navigation bar, click on `OTP Credentials`.
   
   ![Left Side Navigation Bar](./assets/left_side_nav.png)

   You should see your OTP app.

   ![OTP App](./assets/otp_app.png)

4. Hover over the `Actions` dropdown and select `Manage Whitelists`.

   ![Manage Whitelist Dropdown](./assets/manage_whitelists_dropdown.png)

   You should see the table of whitelists of your OTP app.

   ![View Whitelists](./assets/view_whitelists.png)

## Add whitelists to OTP App
1. Make sure you are at the table of whitelists described in the **Viewing whitelists of OTP App** section.
2. Click the `+ Add whitelist(s)` button on the top right.

   ![Add Whitelists Button](./assets/add_whitelists_button.png)

   You should see the form to add whitelists.

   ![Add Whitelists Form](./assets/add_whitelists_form.png)

3. To add an email domain for whitelisting, click on `+Add Email Domain`. A field should popup to enter an email domain. 

   ![Add Email Domain](./assets/add_email_domain.png)

4. You can add more email domains by repeating Step 3. You can remove any email domain by clicking on the bin icon found on the right of every email domain field.
5. To add an user email for whitelisting, click on `+Add User Email`. A field should popup to enter an user email.

   ![Add User Email](./assets/add_user_email.png)

6. You can add more user emails by repeating Step 5. You can remove any user email by clicking on the bin icon found on the right of every user email field.
7. Click on the `Submit` button on the top right. A confirmation prompt should appear asking to proceed with adding the whitelists. Click on `Confirm`.

   ![Add Whitelist Prompt](./assets/add_whitelist_prompt.png)

   A notification should popup saying that the whitelists is successfully added.

   ![Add Whitelist Success Notification](./assets/add_whitelist_success.png)

## Edit whitelist of OTP App
1. Make sure you are at the table of whitelists described in the **Viewing whitelists of OTP App** section.
2. Hover over the `Actions` dropdown and select `Edit`.

   ![Edit Whitelist Dropdown](./assets/edit_whitelist_dropdown.png)

   You should see the form to edit the whitelist.

   ![Edit Whitelist Form](./assets/edit_whitelist_form.png)

3. When editing the whitelist value, take note that it cannot be updated to be of another type. Thus a email domain whitelist cannot be updated to be a user email whitelist and vice-versa.
4. When editing the expiration, do take note that putting a hyphen(`-`) would remove the expiration of the whitelist. Also take note that only future dates are accepted for the expiration.
5. Once done with editing, click on `Submit`. A confirmation prompt should popup asking to proceed with updating the whitelist. Click on `Confirm`.
   ![Edit Whitelist Prompt](./assets/edit_whitelist_prompt.png)

   A notification should popup saying that the whitelists is successfully updated.

   ![Edit Whitelist Success Notification](./assets/edit_whitelist_success.png)

## Delete whitelist of OTP App
1. Make sure you are at the table of whitelists described in the **Viewing whitelists of OTP App** section.
2. Hover over the `Actions` dropdown and select `Delete`.

   ![Delete Whitelist Dropdown](./assets/delete_whitelist_dropdown.png)
3. A confirmation prompt should popup asking to proceed with deleting the whitelist. Enter the whitelist value and click on `Delete`.
   ![Delete Whitelist Prompt](./assets/delete_whitelist_prompt.png)

   A notification should popup saying that the whitelists is successfully deleted.

   ![Delete Whitelist Success Notification](./assets/delete_whitelist_success.png)


