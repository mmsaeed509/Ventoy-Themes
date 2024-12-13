# How to Change the Ventoy Theme

Customizing the appearance of Ventoy involves modifying its configuration file and optionally adding custom theme assets. Follow the steps below to change the theme:

---

## **1. Create or Edit the Theme Directory**

1. **Prepare a Ventoy USB Drive:**
   - Ensure Ventoy is installed on your USB drive.
   - Insert the USB drive and mount it on your system.

2. **Navigate to the Ventoy Partition:**
   - Open the Ventoy partition (often labeled as `VENTOY`).

3. **Create a Theme Folder:**
   - If it doesn't already exist, create a folder named `ventoy` in the root of the partition.
   - Inside the `ventoy` folder, create another folder named `theme`.

---

## **2. Obtain or Customize a Theme**

1. **Download a GRUB2 Theme:**
   - Ventoy themes are based on GRUB2 themes. You can find themes online, such as on [Gnome-Look](https://www.gnome-look.org/).

2. **Place the Theme Files:**
   - Copy the theme folder into the `theme` directory you just created. For example, if the theme is named `mytheme`, its files should be in:
     ```
     /ventoy/theme/mytheme
     ```

---

## **3. Modify the Ventoy Configuration**

1. **Edit the `ventoy.json` File:**
   - In the `ventoy` folder, create or edit the `ventoy.json` file.

2. **Add Theme Configuration:**
   - Include the following JSON snippet, replacing `mytheme` with the name of your theme folder:
     ```json
     {
       "theme": {
         "file": "/ventoy/theme/mytheme/theme.txt",
         "gfxmode": "1920x1080"
       }
     }
     ```
   - Adjust `gfxmode` to match your screen resolution.

---

## **4. Test the Theme**

1. **Safely Eject the USB Drive:**
   - Unmount and eject the drive from your system.

2. **Boot with Ventoy:**
   - Insert the USB drive into your computer and boot from it.
   - Verify that the theme loads correctly.

---

## **5. Troubleshooting**

- **Incorrect Paths:** Ensure the paths in `ventoy.json` match the location of your theme files.
- **Resolution Issues:** If the theme looks off, adjust the `gfxmode` setting to your display resolution.
- **Theme Compatibility:** Some GRUB2 themes may require additional fonts or image formats not supported by Ventoy.

---

By following these steps, you can successfully customize the appearance of your Ventoy boot menu.
