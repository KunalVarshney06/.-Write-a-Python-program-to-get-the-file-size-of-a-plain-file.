# .-Write-a-Python-program-to-get-the-file-size-of-a-plain-file.
import os

def get_file_size(file_path):
    try:
        size = os.path.getsize(file_path)
        return size
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while accessing the file.")

# Example usage
file_path = 'path/to/your/file.txt'  # Replace with the actual file path
file_size = get_file_size(file_path)
if file_size:
    print("File size:", file_size, "bytes")
