# 2026专注 - 部署说明

## 功能特性

- ✅ 目标输入和筛选流程
- ✅ 三步筛选法（所有目标 → 5个 → 3个）
- ✅ 权重分配
- ✅ 生成专注卡壁纸
- ✅ 每日打卡功能
- ✅ Toast 提示消息
- ✅ 演示模式
- ✅ 用户登录/注册
- ✅ 云端数据同步

## 部署步骤

### 1. 配置 Supabase

1. 登录 [Supabase Dashboard](https://supabase.com/dashboard)
2. 打开你的项目：`https://klywwizwconvwjifzrcw.supabase.co`
3. 在 SQL Editor 中执行 `supabase_schema.sql` 创建表
4. 获取 `anon key`：
   - 进入 Settings → API
   - 复制 `anon public` key

### 2. 更新配置

在 `focus2026.html` 中找到第 585 行，将 `YOUR_ANON_KEY_HERE` 替换为实际的 anon key：

```javascript
const SUPABASE_KEY = 'your_actual_anon_key_here';
```

### 3. 部署到服务器

可以使用以下任一方式部署：
- CloudBase（微信云开发）
- EdgeOne Pages
- GitHub Pages
- Vercel
- Netlify

### 4. 测试

1. 打开网页
2. 点击右上角「登录」按钮
3. 注册新账号或登录已有账号
4. 完成目标设置流程
5. 检查右上角同步状态是否正常

## 本地开发

直接在浏览器打开 `focus2026.html` 即可（支持本地存储模式）。

## 注意事项

- Supabase anon key 是公开的，但已配置了行级安全策略
- 用户只能访问自己的数据
- 建议在生产环境中启用邮箱确认
- 可根据需求调整数据库 schema
