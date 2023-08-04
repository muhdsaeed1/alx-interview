A character in UTF8 can be from 1 to 4 bytes long, subjected to the following rules: For 1-byte character, the first bit is a 0, followed by its unicode code. For n-bytes character, the first n-bits are all one's, the n+1 bit is 0, followed by n-1 bytes with most significant 2 bits being 10

In python code, add sys.stdout.reconfigure(encoding="utf-8")
By environment variable. Set PYTHONIOENCODING to "utf-8"
By environment variable. Set PYTHONUTF8 to 1.
By python command option: -X utf8


