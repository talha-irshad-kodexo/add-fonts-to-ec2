# Add Custom Fonts to your AWS EC2 Instance
This is a tutorial on how you can add custom fonts to you AWS EC2 instance.
## Why:
EC2 instance does not include custom fonts like sans-serif, Poppins on its own therefore we need to add them seperately
## Steps:
Here are the steps for adding Poppins font to you EC2. Change the Link and folder names according to your desired font:
- Connect to you EC2 instance via SSH
- Copy the download link of the zip archive of the font of your choice
- Run `wget https://fonts.google.com/download?family=Poppins` to download the zip compressed font files.
- Run `unzip download?family=Poppins` where `download?family=Poppins` is the file name of the zip file downloaded.
- Run `sudo mkdir -p /usr/share/fonts/poppins` to make a folder for the font of your choice.
- Run `sudo mv *.ttf /usr/share/fonts/poppins` to move the extracted .ttf files to the folder you made earlier.
- Run `fc-cache -r` to add the newly added font to cache.

**You are all set.**
Now you can use these fonts in your nodeJS, python or any server that is running on you EC2 instance.

### Tip:
You can use `ls` command to check the contents of the extracted folder or the file name of the downloaded file
