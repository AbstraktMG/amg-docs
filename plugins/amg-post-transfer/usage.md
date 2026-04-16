---
title: Usage
parent: Post Migration
grand_parent: Plugins
nav_order: 3
---

# Usage

## Where to find it

**WordPress Admin → AMG → Post Migration**

You'll see two tabs: **Export** and **Import**.

---

## Exporting posts (from Site A)

### Step 1: Choose what to export

1. Open the **Export** tab
2. Use the **post type dropdown** to pick what kind of content you want — Posts, Pages, Products, etc.
3. The list below shows everything of that type on the site
4. Use the **search box** to filter by title if the list is long

### Step 2: Pick your media option

Next to the post type dropdown, choose how to handle images:

- **Bundle media in ZIP** *(recommended)* — Includes all images, PDFs, and other media files inside the ZIP. Bigger file, but everything imports cleanly even if the source site goes offline.
- **Leave URLs (download on import)** — Skips the media files. The destination site will try to download images from the original URLs during import. Smaller ZIP, but only works if the source site is still live and accessible.

> **Designer tip:** Always pick "Bundle media" unless the export ZIP is getting too big to upload (over ~100 MB).

### Step 3: Select posts

- Check the boxes next to the posts you want
- Use the **header checkbox** to select everything currently visible on the page
- Use the **"All Posts" checkbox** (next to the Title column) to select every post across every page — useful for big exports

### Step 4: Export

1. Click **Export Selected Posts**
2. A progress bar appears — exports happen in chunks, so large jobs may take a minute or two
3. When it finishes, the ZIP file downloads automatically to your computer
4. Save it somewhere you'll remember (Desktop or Downloads)

---

## Importing posts (to Site B)

### Step 1: Open the Import tab

Go to **AMG → Post Migration → Import**.

### Step 2: Upload your ZIP

1. Drag and drop your `.zip` file into the dropzone, or click to browse
2. Wait for "Processing ZIP..." to finish
3. A **preview** appears showing:
   - How many posts are in the file
   - What types of posts they are
   - How many media files are included
   - Which site they came from

> **Sanity check:** If the numbers look wrong (e.g., 2 posts when you expected 50), the wrong file got uploaded.

### Step 3: Choose import settings

**Assign Author**
- Pick which user account should "own" the imported posts on this site
- If the original author doesn't exist on the new site, this is who gets credited
- Defaults to the current user

**Post Type Mapping**
- After uploading, a mapping section appears for each source post type
- Default is to keep the same type (page → page, product → product)
- Switch any type to a different registered post type on the destination (e.g., page → case_study)

**Duplicate Handling** — What happens if a post with the same slug already exists?

- **Skip duplicates** *(default, safest)* — Leaves existing posts alone, only imports new ones
- **Update duplicates** — Overwrites existing posts with the imported version. Cannot be undone.
- **Import as new posts** — Always creates new posts, even if it makes a duplicate. WordPress will adjust the slug (e.g., `about-us-2`)

### Step 4: Run the import

1. Click **Import Posts**
2. Watch the progress bar — posts import one at a time
3. The **Import Log** shows each post as it processes (Imported, Skipped, Failed)
4. When it finishes, your posts are live on the new site
