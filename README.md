# mini-os

# Tạo release
gh release create v2.0 releases/minios-chroot.tar.gz releases/mini-os.iso  --title "MiniOS v1.0" --notes "Initial mini system"

# Xóa file cũ trong release
gh release delete-asset v2.0 releases/minios-chroot.tar.gz

# Upload file mới
gh release upload v2.0 releases/minios-chroot.tar.gz releases/mini-os.iso --clobber

// giải nén file squashfs
sudo unsquashfs -d build/chroot releases/filesystem.squashfs