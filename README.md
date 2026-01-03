File Organizer
A simple Python script that cleans up messy directories by automatically organizing files into categorized folders.

What It Does
This tool helps you tame chaotic download folders or any directory that's gotten out of hand. It :-

Renames files with timestamps to avoid duplicates
Removes special characters from filenames (replaces with underscores)
Sorts files into folders based on type:

Images (jpg, png, gif, etc.)
Documents (pdf, docx, txt, etc.)
Videos (mp4, mov, avi, etc.)
Archives (zip, rar, 7z)
Others (anything that doesn't fit)



Requirements

Python 3.6 or higher
No external dependencies (uses standard library only)

Installation
bashgit clone https://github.com/vyanmadai7/file-organizer.git
cd file-organizer
Usage
Just run the script and enter the path to the directory you want to organize:
bashpython file_organizer.py
When prompted, enter the full path:
The script will:

Scan all files in the directory
Rename them with clean names and timestamps
Create category folders if they don't exist
Move files into their appropriate folders

----------:EXAMPLE:----------

Before:
Downloads/
├── vacation photo (1).jpg
├── report@final_FINAL.pdf
├── movie 2023.mp4
└── random-file.txt
After:
Downloads/
├── Images/
│   └── vacation_photo__1__20250101-143022.jpg
├── Documents/
│   ├── report_final_FINAL_20250101-143023.pdf
│   └── random_file_20250101-143024.txt
└── Videos/
    └── movie_2023_20250101-143025.mp4
Adding New File Types
Edit the file_types dictionary in the code to add more categories:
pythonfile_types = {
    'Images': ['.jpg', '.jpeg', '.png', '.gif', '.bmp'],
    'Audio': ['.mp3', '.wav', '.flac'],  # Add your own
    # ... more types
}
Safety Notes

Test it first on a non-critical directory
The script renames and moves files - make sure you have backups
Subfolders in the target directory are ignored (not organized)
Logs show exactly what's happening in case something goes wrong

Contributing
Feel free to open issues or submit pull requests if you have ideas for improvements!
License
MIT License - do whatever you want with it.
