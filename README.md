# Hướng dẫn cài đặt 0G-DA-Node

## Yêu cầu hệ thống
| Thể loại | Yêu cầu |
| ------------ | ------------ |
| CPU | 2+ lõi |
| RAM | 8+ GB |
| Băng thông | 100 MBps để Tải xuống / Tải lên |

### Cập nhật hệ thống
```búa
sudo apt-get cập nhật
sudo apt-get install git cargo clang cmake build-essential pkg-config openssl libssl-dev protobuf-compiler
```
### Cài đặt Go
```búa
cd $HOME && \
phiên bản="1.22.0" && \
wget "https://golang.org/dl/go$ver.linux-amd64.tar.gz" && \
sudo rm -rf /usr/local/go && \
sudo tar -C /usr/local -xzf "go$ver.linux-amd64.tar.gz" && \
rm "go$ver.linux-amd64.tar.gz" && \
echo "xuất PATH=$PATH:/usr/local/go/bin:$HOME/go/bin" >> ~/.bash_profile && \
nguồn ~/.bash_profile && \
phiên bản đi
```
### Git Clone Mã Nguồn
```búa
git clone -b v1.0.0-testnet https://github.com/0glabs/0g-da-client.git
```
### Chạy
```búa
cd ~/0g-da-client
làm xây dựng
```

### Chạy máy chủ kết hợp

<thay đổi đầu vào>
 
Cấu hình `run_combined`

```búa
cd ~/0g-da-client/disperser
```
```búa
nano Makefile
```
Tìm run_combined sau đó làm theo chỉnh sửa bên dưới \
--chain.rpc https://rpc-testnet.0g.ai \
--chain.private-key <Khóa_riêng_của_bạn> \
--combined-server.storage.node-url http://0..0.0.0:5678 \ nếu bạn có nút lưu trữ url \
--combined-server.storage.flow-contract 0x8873cc79c5b3b5666535C825205C9a128B1D75F1 \

### Chạy
```búa
thực hiện run_combined
```
 
### Nhật ký cũ
```búa
THÔNG TIN [07-16|15:37:55.210|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:155] [encodingstreamer] đang yêu cầu xử lý blob.. caller=encoding_streamer.go:155
THÔNG TIN [07-16|15:37:55.210|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:170] [encodingstreamer] không có siêu dữ liệu mới để mã hóa caller=encoding_streamer.go:170
THÔNG TIN [07-16|15:37:56.458|github.com/0glabs/0g-data-avail/disperser/apiserver/server.go:414] [apiserver] số khối mới nhất đã hoàn thiện số cập nhật=278,402 người gọi=server.go:414
THÔNG TIN [07-16|15:37:57.210|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:155] [encodingstreamer] đang yêu cầu xử lý blob.. caller=encoding_streamer.go:155
THÔNG TIN [07-16|15:37:57.211|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:170] [encodingstreamer] không có siêu dữ liệu mới nào để mã hóa caller=encoding_streamer.go:170
THÔNG TIN [07-16|15:37:59.210|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:155] [encodingstreamer] đang yêu cầu xử lý blob.. caller=encoding_streamer.go:155
THÔNG TIN [07-16|15:37:59.210|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:170] [encodingstreamer] không có siêu dữ liệu mới để mã hóa caller=encoding_streamer.go:170
THÔNG TIN [07-16|15:38:00.210|github.com/0glabs/0g-data-avail/disperser/batcher/batcher.go:193] [batcher] Tạo lô ts=2024-07-16T15:38:00+0000 caller=batcher.go:193
THÔNG TIN [07-16|15:38:01.210|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:155] [encodingstreamer] đang yêu cầu xử lý blob.. caller=encoding_streamer.go:155
THÔNG TIN [07-16|15:38:01.210|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:170] [encodingstreamer] không có siêu dữ liệu mới để mã hóa caller=encoding_streamer.go:170
THÔNG TIN [07-16|15:38:01.462|github.com/0glabs/0g-data-avail/disperser/apiserver/server.go:414] [apiserver] số khối mới nhất đã hoàn thiện số cập nhật=278,403 người gọi=server.go:414
THÔNG TIN [07-16|15:38:03.210|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:155] [encodingstreamer] đang yêu cầu xử lý blob.. caller=encoding_streamer.go:155
THÔNG TIN [07-16|15:38:03.210|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:170] [encodingstreamer] không có siêu dữ liệu mới để mã hóa caller=encoding_streamer.go:170
THÔNG TIN [07-16|15:38:05.210|github.com/0glabs/0g-data-avail/disperser/batcher/batcher.go:193] [batcher] Đang tạo lô ts=2024-07-16T15:38:05+0000 caller=batcher.go:193
THÔNG TIN [07-16|15:38:05.210|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:155] [encodingstreamer] đang yêu cầu xử lý blob.. caller=encoding_streamer.go:155
THÔNG TIN [07-16|15:38:05.210|github.com/0glabs/0g-data-avail/disperser/batcher/encoding_streamer.go:170] [encodingstreamer] không có siêu dữ liệu mới để mã hóa caller=encoding_streamer.go:170
THÔNG TIN [07-16|15:38:06.466|github.com/0glabs/0g-data-avail/disperser/apiserver/server.go:414] [apiserver] số khối mới nhất đã hoàn thiện số cập nhật=278,403 người gọi=server.go:414
```

```

 
