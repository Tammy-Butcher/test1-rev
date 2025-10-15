---
title: Add and Manage Categories
excerpt: Design your classification system for videos using Rev's category feature
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Categories and subcategories are used to create a classification system for your content. Users will only see a category if they have access to at least one video in it. 

> 📘 Note
>
> There are three [roles](doc:roles-and-permissions) in Rev that can create and manage categories and sub-categories: **Account Admin**, **Media Admin**, and **Category Creators**.
>
> **Category Creators** can only edit the categories they create from the [Browse Categories](doc:user-menu-options#videos) menu.

<Image title="categories.png" alt={902} align="center" src="https://files.readme.io/ccc7c90-categories.png">
  Use the Categories form to create both new categories and subcategories
</Image>

To create both categories and subcategories (Admin roles):

1. Navigate to **Admin > Media Settings > Categories**.

2. Enter a **Category Name** in the **New Category** field and click **Create** to add a new category or click an existing category to edit it.

3. Click the **Add Subcategory** button next to a **Category Name** to add a subcategory to the category.

4. Keep in mind each category and subcategory name must be unique within each category hierarchy.

5. Click and drag a category to rearrange it.  The **plus** and **minus** icons expand a category tree to display the subcategories it contains (if any).  

6. The **Items** column displays the number of videos assigned to that category.

7. The **Restricted** column displays (at a glance) if the category is secure which means that it is restricted to specific users and groups that you specify.

> 👍 Tip
>
> If you are an Admin or the Category creator, you can also quickly edit a category from the **Browse Categories** screen by clicking the **Edit** button (list view) or **Settings** gear (Grid view).

## Add a Thumbnail to a Category

You can provide visual previews to your categories by attaching a thumbnail image to them.  Once the category is created this feature is available.

1. Click on the category name to edit it.
2. Click the **Upload** button and select an image to use as your thumbnail.  For best results, select an image that is approximately 480x360.

<Image align="center" src="https://files.readme.io/53f0a4c-addThumbnailtoCategory.png" />

3. Make sure to click the **Save Category** button.
4. Thumbnails display in both grid and list view.  If a thumbnail has not been applied, a placeholder default folder image is used instead.

<Image align="center" src="https://files.readme.io/8d734cb-categoriesGridView.png" />

5. You can also add or edit the thumbnail of a category (including the uncategorized category) from the **Browse Categories** page by clicking the gear icon under the category.

<Image alt="Edit category features by clicking the Gear icon on the Browse Categories page" align="center" src="https://files.readme.io/d61bd2bb6e6a0dd52fbaf582876bbffed8ae635d241be149b211b89135f6af60-categoryGear.png">
  Edit category features by clicking the Gear icon on the Browse Categories page
</Image>

## Create a Secure Category

Rev allows you to assign permissions to categories which means you can restrict the users and groups that may add content to them. 

> 👍 Tip
>
> When you create a **Secure Category**, its use is restricted to specific users and groups; as a result, the terms "Secure Category" and "Restricted Category" are sometimes used interchangeably.

Permissions can be assigned to your categories. A **Category Manager** permission can be assigned within the category (seen below) and is responsible for managing categories and subcategories while the **Category Contributors** can add content to it.

A Rev system-wide **Category Creator** role allows a user account to create new top-level categories while leaving the day-to-day operation of the category to the manager and contributor permissions that you define for it.

<Image title="addSecureCategory.jpg" alt={902} align="center" src="https://files.readme.io/b3e77d6-addSecureCategory.jpg">
  Enable the Restricted checkbox to create a Secure Category and add users and groups. Then assign the permissions to them to manage it.
</Image>

To create a Secure Category:

1. Click the **Restricted** checkbox under **Permissions**.

2. Enter a User or Group in the **Find Items** control and click **Done**.

3. Assign either a **Category Manager** or **Category Contributor** permission.
   * **Category Managers** can edit the **Category Name** and add subcategories; **Category Contributors** can only add content. You should designate at least *one* Category Manager for every Secure Category you create.

4. Click **Save Category** to add the new Secure Category.

## Delete a Category or Subcategory

1. Navigate to **Media Settings > Categories**.

2. Click the **Delete** icon next to the category or subcategory you want to delete.

3. Deleting a category also deletes its subcategories.

4. Videos associated with deleted categories and subcategories are disassociated but *not* deleted.
