#!/bin/bash
# Step 1: Create a file
echo "Creating file: demo_script.sh"
touch demo_script.sh

# Step 2: Show initial permissions
echo "Initial permissions:"
ls -l demo_script.sh

# Step 3: Assign permissions using symbolic notation
echo "Setting permissions using symbolic notation: u=rwx, g=rx, o=rx"
chmod u=rwx,g=rx,o=rx demo_script.sh
ls -l demo_script.sh

# Step 4: Change permissions using numeric (octal) notation
echo "Changing permissions to 750 (rwxr-x---)"
chmod 750 demo_script.sh
ls -l demo_script.sh

# Step 5: Remove execute permission for group and others
echo "Removing execute permission for group and others (symbolic)"
chmod go-x demo_script.sh
ls -l demo_script.sh

# Step 6: Set permissions to 644 (rw-r--r--)
echo "Setting permissions to 644 (rw-r--r--)"
chmod 644 demo_script.sh
ls -l demo_script.sh

echo "Done."
