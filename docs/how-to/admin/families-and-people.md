---
status: needs-ui
primary: frontend
---

<!-- @backend verified: a "community" IS a family (1:1 merge); the family is the WrapAround
     care circle. Family records hold parents and children; one parent is the primary contact.
     CSV import of families is supported and every import is written to the audit log. -->

# Manage families & people

**Who this is for:** Program staff (Admins and Coordinators); advocates for their church's
families.
**When to use it:** When you set up a new family or update who's in one.
**Before you start:** You're signed in with staff access.

![The Families directory, as Central Admin.](../../assets/screens/admin-families.png)

## The family is the care circle

In AlignOne a **family** *is* the WrapAround care circle — everything else is organized
around it. A family record holds its **parents** and **children**, with one parent set as
the **primary contact**. Each family also contains lots of information regarding the family and how they can be served.

## Add a family - Admin only
**NOTE:**
While working in this new family page your changes will be saved as you go. This means you can refresh, navigate to other pages or tabs to look up information and when you return your changes will still be there. There will be a small message at the top of the page saying "Restored your unsaved draft from 9:19 PM. Nothing has been created yet." This prompt will have a option to clear all fields. If you want to discard all of your changes instead of having them saved as a draft, go to the bottom of the page and click cancel. The information you have filled in is saved locally in your browser, it will survive a refresh, but it will **not** survive closing and re-opening the tab.

1. Open **Families** and choose **New Family**.
2. Fill in, at minimum, the **Family Name** and **Primary Contact** information.
	- **Family Name** This is not forced as a unique value, but ideally you don't want duplicate family names. You will be warned if the family name you have entered is a duplicate. Current best practice is to use the first and last name of the primary contact.
	- **Primary Contact** means adding a parent with a name, email address, and checking the primary contact checkbox.
	- **NOTE:** The **Create Family** button will be disabled until you have entered at least these two items.
3. Clicking on **Create Family** will create the family, save all your entered data, and then take you directly to the new family page.
![The New Family form.](../../assets/screens/admin-new-family-modal.png)  <!-- This photo is out of date. Need a new picture from the @frontEnd -->

## Update a family

1. Open the family from **Families**.
2. Click on **Edit Details** in the top right.
3. Make any changes you want.
4. **Save** your changes by clicking **Save changes** in the top right.

## Family photo

### Adding or Updating a photo
1. Open the family,
   - if the family has no photo hover over the photo box and click **Add**.
   - if the family has a out of date photo, Hover over the existing photo and click **Change**.
2. Choose the new image and confirm to upload.

### Removing a family photo
1. Open the Family.
2. Hover over the family photo and click remove.

!!! warning "Never use real PII in examples or templates you share"
    Family information is sensitive. Keep any exported or filled-in CSV files secure and out
    of shared locations.

## Related

- [Manage volunteers & advocates](volunteers-and-advocates.md)
- [Onboard a family & invite people](onboarding.md)
- [Manage churches & counties](organizations.md)
- [Oversight](oversight.md)
