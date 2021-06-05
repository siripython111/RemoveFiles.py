import time
import os
import shutil
def main ():
 deleted_folder_count = 0
 deleted_file_count = 0
 path = "C:/Users/Baby/Desktop/wendy"
 seconds = time.time() - (days*24*60*60)
 if os.path.exists(path):
  for root_folder, files, folders in os.walk(path)
   if seconds >= get_file_or_folder_age(root_folder):
    remove_folder(root_folder)
    deleted_folder_count += 1
    break
   else:
    for folder in folders:
     folder_path = os.path.join(root_folder, folder)
     if seconds >= get_file_or_folder_age(folder_path):
   def get_file_or_folder_age(path):
    ctime = os.stat(path).st_time
    return ctime
  main()
