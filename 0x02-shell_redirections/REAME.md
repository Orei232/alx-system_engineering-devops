echo "Hello World" prints out Hello world
echo "\""(Ôo)' -- displays contents in confused smiley
cat /etc/passwd -- displays contents of /etc/passwd
cat /etc/passwd/etc/hosts -- displays contents of /etc/passwd/etc/hosts
tail -n 10 /etc/passwd -- displays the last ten lines of /etc/passwd
head -n 10 /etc/passwd -- displays the first ten lines of /etc/passwd
head -n 3 lacta | tail -n 1 --  displays the third line of the file lacta
echo "Best School" > \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) will create a file named \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing "Best School" ending by a new line
ls -la > ls_cwd_content -- writes into the file ls_cwd_contentthe result of ls -la
tail -n 1 lacta >> lacta -- duplicates the last line of the file lacta
find .name "*js" -type f -delete -- deletes all regular files with a .js
ls -t | head -- counts the number of directories and sub-directories in the current directory
ls -l n-10  -- displays the ten newest files in a directory
sort | uniq -u takes a list of words as input and prints only words that appear exactly once
grep "root" /etc/passwd -- displays lines containing the pattern “root” from the file
grep -c "bin' /etc/passwd -- displays the number of lines that contain the pattern “bin” in the file

