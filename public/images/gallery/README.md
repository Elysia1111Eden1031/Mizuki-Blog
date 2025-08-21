# 相册图片目录说明

这个目录用于存放相册页面的图片文件。请按照以下结构组织您的图片：

## 推荐目录结构

```
public/images/gallery/
├── travel-cover.jpg          # 旅行相册封面图
├── travel-1.jpg              # 旅行相册图片1
├── travel-2.jpg              # 旅行相册图片2
├── travel-3.jpg              # 旅行相册图片3
├── daily-cover.jpg           # 日常相册封面图
├── daily-1.jpg               # 日常相册图片1
├── daily-2.jpg               # 日常相册图片2
├── food-cover.jpg            # 美食相册封面图
├── food-1.jpg                # 美食相册图片1
├── food-2.jpg                # 美食相册图片2
├── food-3.jpg                # 美食相册图片3
└── food-4.jpg                # 美食相册图片4
```

## 使用说明

1. **添加图片**：将您的图片文件复制到此目录
2. **配置相册**：编辑 `src/pages/gallery.astro` 文件中的 `galleryGroups` 数组
3. **更新路径**：确保配置中的图片路径与实际文件路径匹配

## 图片要求

- **格式**：支持 JPG、PNG、WebP 等常见格式
- **尺寸**：建议封面图片至少 800x600 像素
- **命名**：使用英文和数字，避免特殊字符和空格

## 示例配置

在 `src/pages/gallery.astro` 中：

```javascript
const galleryGroups = [
  {
    id: 1,
    title: '我的旅行',
    description: '记录美好的旅行时光',
    coverImage: '/images/gallery/travel-cover.jpg',
    imageCount: 3,
    createdAt: '2024-01-15',
    tags: ['旅行', '风景'],
    images: [
      '/images/gallery/travel-1.jpg',
      '/images/gallery/travel-2.jpg',
      '/images/gallery/travel-3.jpg'
    ]
  }
];
```

注意：图片路径以 `/images/gallery/` 开头，这对应 `public/images/gallery/` 目录。