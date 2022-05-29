# PythonSearchFiles
Script to search files in multiple directories and copy the result to the clipboard

The following items need to be defined by the user:

| Step | Variable | Comment |
| ---- | -------- | ------- |
|  1   | START_LOCATION | Indicates in which directory the seach starts <br> os.getcwd() indicates the current work directory <br> stating with r" allows to copy the path literally |
|  2   |  MAX_DEPTH | Indicates how deep the search tree will be |
|  3   |  def Requirement(direntry) | Indicates which files need to be included in the search report |
|  4   |  SORT | Indicates how the files are sorted |
|  5   |  SORT_REVERSE | Indicates if he sort order is ascending (False) or descending (True) |
|  6   |  COLUMNS | Indicates which columns need to be exported |

The following tags are available for steps 4 and 6:

| TAG      | Meaning |
|----------|---------|
| Name     | Filename                                            |
| Path     | Path, including filename                            |  
| Size     | Filesize                                            |
| Created  | Date and time when the file was created             |
| Modified | Date and time when the file was last modified       |
| Accessed | Date and time when the file was last accessed       |
| Exifdate | For photo's: Date and time when the photo was taken |
| Width    | For images: the width of the image in pixels        |
| Height   | For images: the height of the image in pixels       |



This script uses the following libraries:
|    |      |
|----|------|
| exifread  | to import exif data (date, width, height) from Exif data of photo's |
| Pillow    | to import data from photo's if exifread fails |
| pyperclip | to export the results to the clipboard |

These libraries are only called if needed (if no photo data is requested, libraries do not need to be installed)
