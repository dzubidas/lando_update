# Drupal Environment Management Script
This repository contains a shell script to manage and update a Drupal environment using Lando. The script automates several tasks necessary for maintaining a Drupal site, including updating Composer dependencies, clearing caches, importing configuration changes, and applying database updates.

## Prerequisites
- [Lando](https://docs.lando.dev/basics/installation.html) installed
- A Drupal project set up in a Lando environment

## Script Breakdown
Here’s a detailed breakdown of what the script does:

1. **lando composer self-update**
   Updates Composer to the latest version.

2. **lando composer install**
   Installs the Composer dependencies defined in your composer.json file.

3. **lando drush cr**
   Clears the Drupal cache to ensure all changes are recognized.

4. **lando drush cim -y**
   Imports configuration changes from your configuration files into the Drupal database.

5. **lando drush cr**
   Clears the Drupal cache again to ensure configuration changes are fully applied.

6. **lando drush updb**
   Applies any pending database updates.

7. **lando drush cr**
   Clears the Drupal cache one last time to finalize the update process

## Notes
- The script includes a commented-out line for updating the Composer lock file. Uncomment it if you need to update the lock file.

## Contributing
- If you have suggestions or improvements, feel free to create a pull request or open an issue.
