# cyberspace008
wordpress malware scanner in php

# wp-malware-scanner
PHP script to scan WordPress databases for hidden malware in the wp_options table, detecting common malicious code patterns.

# WordPress Malware Scanner Script

This PHP script scans your WordPress database for suspicious entries in the `wp_options` table. It looks for common patterns in malicious code such as `<script>`, `eval`, `base64_decode`, and `document.write`.

## How to Use

### Step 1: Download and Edit the Script

1. Download the `scanner.php` script or copy the code from [here](scanner.php).
2. Open the `scanner.php` file in any text editor.
3. Replace the following placeholders with your database credentials:
   - `your_db_host`: Your database host (e.g., `localhost`).
   - `your_db_username`: Your database username.
   - `your_db_password`: Your database password.
   - `your_db_name`: Your WordPress database name.

### Step 2: Upload the Script

1. Upload `scanner.php` to the root of your WordPress installation directory (or any directory accessible on your web server).

### Step 3: Run the Script

You can run the script in two ways:

#### Option 1: Via Web Browser
1. Navigate to the script’s location in your browser, e.g., `http://yourwebsite.com/scanner.php`.
2. The script will output any suspicious entries it finds in the `wp_options` table.

#### Option 2: Via SSH
1. SSH into your server.
2. Run the script using the following command:
   ```bash
   php /path/to/scanner.php
   ```

### Step 4: Review the Results

If suspicious entries are found, the script will display the option name and the first 300 characters of the option value for review. You can then manually investigate and clean the database as necessary.

### Step 5: Clean Up

Once you've completed your scan:
- **Delete the `scanner.php` file** from your server to prevent unauthorized access.

## Important Notes

- **Security**: This script only reads your database and does not make any modifications. It's up to you to manually clean any suspicious entries it finds.
- **Backup**: Always make sure you have a backup of your database before making any changes to it.

## Disclaimer

This script is provided as-is without any warranty. Use at your own risk. The script is a simple scanner meant to assist with the detection of known malicious patterns, but it may not detect all forms of malware or malicious code.

