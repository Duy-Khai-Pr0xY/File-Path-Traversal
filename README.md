# File-Path-Traversal

# Unsafemethot 
  ### readfile(untrusted_data) 
  ### file_put_contents(untrusted_data)
  ### include untrusted_data
  ### ........
# Unsafemethot + untrusted_data = vỡ mồm
# include trong php là read and excute
# include(untrusted_data) + kiểm soát nội dung file = RCE
### có thể double percent-encoded ..%252f..%252f..%252fetc/passwd -> phân giải ra ..%2f..%2fetc/passwd -> ../../etc/passwd
### sử dụng null buyte (%00,\0,...) -> vd: shell.php%00.png -> shell.php (từ phiên bản php 5.3+ là bị loại bỏ)
