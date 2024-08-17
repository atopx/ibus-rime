# 自用linux中文输入法配置

- Ubuntu/debian全系列
- gnome桌面环境

![截图 2024-08-17 10-47-28](https://github.com/user-attachments/assets/b429da78-da6a-4a95-a5cb-7f951e00b855)


## 安装

```bash
sudo apt install -y ibus-rime
mkdir -p $HOME/.config/ibus
git clone git@github.com:atopx/ibus-rime.git $HOME/.config/ibus/ibus
```

## 启用rime

设置 -> 键盘 -> 输入源 -> 添加输入源 -> 中文(Rime)
Settings -> Keyboard -> Input Source -> Add Input Source -> Chinese(Rime)
