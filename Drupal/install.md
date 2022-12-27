# Create New Drupal project from scratch

## Download Composer - If not downloaded. If downloaded, skip this step.
  ### Composer installation - https://getcomposer.org/download
  ### Starting a Site Using Drupal Composer Project Templates - https://www.drupal.org/docs/develop/using-composer/starting-a-site-using-drupal-composer-project-templates 

#### 1. Install drupal project template using Composer.
> `composer create-project drupal/recommended-project bsv_academy`

#### 2. Go to the created project folder.
> `cd bsv_academy`

Lando Installation - https://docs.lando.dev/config/drupal9.html#configuration

#### 3. Initialize a drupal9 recipe using the latest drupal 9 version

> `lando init \
  --source remote \
  --remote-url https://www.drupal.org/download-latest/tar.gz \
  --remote-options="--strip-components 1" \
  --recipe drupal9 \
  --webroot web \
  --name bsv_academy`
  
#### 4. Start the lando
> `lando start`

#### List information about this app.
> `lando info`

#### 5. Install drush using composer
Go inside lando container.
> `lando ssh`

#### Install drush
> `composer require drush/drush`

#### 6. lando site-install
> `lando drush site-install standard --db-url='mysql://drupal9:drupal9@database/drupal9' --site-name='bsv_academy' --yes`

### Use the username and password to login to the drupal site.

-------------- Ready to Go ---------------
