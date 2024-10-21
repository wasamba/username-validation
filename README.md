#! /bin/bash
#samba figueiredo
# username.sh
echo "Enter a valid username: "
read -r username

# Loop until a valid username is entered
while ! echo "$username" | grep -E "^[a-z][a-z0-9_]{2,11}$" > /dev/null 2>&1
do
    echo "Invalid username! Username must start with a lowercase letter, can only contain lowercase letters, digits, or underscores, and must be between 3 and 12 characters long."
    echo "Enter a potential username: "	
    read -r username
done

echo "Thank you!"
