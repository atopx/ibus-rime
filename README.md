# 自用linux中文输入法配置

- Ubuntu/debian全系列
- gnome桌面环境

![截图 2024-08-17 10-47-28](https://github.com/user-attachments/assets/b429da78-da6a-4a95-a5cb-7f951e00b855)


## 安装

```bash
sudo apt update
sudo apt install -y fcitx5 fcitx5-chinese-addons fcitx5-frontend-gtk3 fcitx5-frontend-gtk4 fcitx5-frontend-qt5 fcitx5-module-cloudpinyin fcitx5-rime
im-config -n fcitx5

echo "GTK_IM_MODULE DEFAULT=fcitx5" >> ~/.pam_environment
echo "QT_IM_MODULE DEFAULT=fcitx5" >> ~/.pam_environment
echo "XMODIFIERS DEFAULT=\@im=fcitx5" >> ~/.pam_environment
echo "SDL_IM_MODULE DEFAULT=fcitx5" >> ~/.pam_environment

mkdir -p $HOME/.local/share/fcitx5
git clone -b fcitx5 git@github.com:atopx/ibus-rime.git $HOME/.local/share/fcitx5/rime --depth 1

```


## 需要注销/重新登录

```bash
fcitx5-configtool # 从右侧可用输入法中选择“中州韵” 添加到左侧
```

## 全局选项选项配置

输入法选择
![alt text](docs/image1.png)


快捷键配置
![alt text](docs/image2.png)


主题/字体配置
![alt text](docs/image3.png)

## 部署

输入法托盘菜单点击重新启动，等待自动部署

## 自启动

![alt text](docs/image4.png)
