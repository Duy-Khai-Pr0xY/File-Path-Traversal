# File-Path-Traversal

# Unsafemethot 
  ### readfile(untrusted_data) 
  ### file_put_contents(untrusted_data)
  ### include untrusted_data
  ### ........
# Unsafemethot + untrusted_data = vỡ mồm
# include trong php là red and excute
# include(untrusted_data) + kiểm soát nội dung file = RCE
### có thể double percent-encoded
