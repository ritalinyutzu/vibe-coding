# 🎨 共感工作室 (Vibe Coding)

音樂 × 藝術 × 實時視覺化

## 📖 專案簡介

**共感工作室** 是一個網頁式音樂視覺化應用，可以將妳喜歡的音樂轉化為令人驚艷的視覺效果。上傳任何 MP3 或 WAV 檔案，選擇 12 種視覺風格之一，然後享受由音樂驅動的動態藝術。

### ✨ 核心功能

- 🎵 **本地音樂播放** - 支援 MP3、WAV 等音訊格式
- 📊 **實時音頻分析** - FFT 頻譜分析驅動視覺化
- 🎨 **12 種視覺風格** - 從霓虹故障到分形藝術
- 🖼️ **背景圖片支援** - 上傳圖片作為視覺背景
- 🔄 **3D 圖片旋轉** - 四軸旋轉控制（X、Y、Z + 不旋轉）
- ⚙️ **參數調整** - 節拍敏感度、顏色飽和度、效果強度、動畫速度
- 🌈 **白色極簡介面** - 繁體中文完全本地化

---

## 🚀 快速開始

### 方式 1️⃣：線上使用
訪問：[https://vibe-coding-6kze4il1k-ritalinyutzus-projects.vercel.app](https://vibe-coding-6kze4il1k-ritalinyutzus-projects.vercel.app)

### 方式 2️⃣：本地執行

1. **複製倉庫**
```bash
git clone https://github.com/yourusername/vibe-coding.git
cd vibe-coding
```

2. **打開應用**
```bash
# 用任何本地伺服器打開 index.html
# 推薦使用 Python：
python -m http.server 8000

# 或使用 Node.js http-server：
npx http-server
```

3. **訪問**
在瀏覽器打開：`http://localhost:8000`

---

## 📋 使用步驟

### 步驟 1️⃣：上傳音樂
- 點擊「📤 選擇音樂 (MP3/WAV)」
- 選擇妳喜歡的音樂檔案
- 檔案名稱會顯示在面板上

### 步驟 2️⃣：調整音量（可選）
- 使用音量滑塊調整音樂大小
- 預設設定為 70%

### 步驟 3️⃣：上傳背景圖片（可選）
- 點擊「🖼️ 上傳圖片」
- 選擇想要的背景圖片
- 圖片會顯示在視覺化背景中

### 步驟 4️⃣：選擇視覺風格
點擊 12 種視覺風格中的任何一種：
- 🔦 **霓虹故障** - 8 條彩色發光線條
- 💧 **流動液態** - 藍色發光球體旋轉
- 🔷 **幾何波紋** - 12 個彩色八面體環形
- ✨ **能量粒子** - 1500 個彩色粒子
- 📊 **頻譜柱狀** - 32 根彩虹柱子
- 〰️ **漣漪波動** - 彩色網格波紋
- 🌀 **旋轉螺旋** - 彩虹球體螺旋
- 🌌 **光軌跡** - 5 條發光管道
- 🌠 **星光隧道** - 星光通道視覺
- 🎭 **分形藝術** - Mandelbrot 集合
- ⚡ **電漿效應** - 波形合成動畫
- 🌊 **圖片波動** - 圖片 + 動態波紋

### 步驟 5️⃣：調整參數
在「⚙️ 參數調整」區域：
- **🎯 節拍敏感度** (1-100%) - 視覺化對音樂的反應強度
- **🌈 顏色飽和度** (1-100%) - 顏色的鮮豔程度
- **💥 效果強度** (1-100%) - 視覺變化的幅度
- **⚡ 動畫速度** (1-100%) - 所有動畫的快慢

### 步驟 6️⃣：圖片旋轉控制（可選）
- 選擇旋轉軸：X軸、Y軸（迷因貓貓推薦）、Z軸、不旋轉
- 調整旋轉速度：0.1x - 5.0x
- 勾選「播放時自動旋轉」自動旋轉

### 步驟 7️⃣：開始播放
- 點擊「▶️ 開始播放」開始播放音樂和視覺化
- 點擊「⏸️ 暫停」暫停

---

## 🎨 視覺風格詳解

### 3D 風格（10 種）
使用 Three.js 渲染，圖片作為背景顯示在效果後面：
- 包含光源、材質、發光效果
- 實時音頻驅動動畫
- 支援所有參數調整

### 2D 風格（3 種）
使用 Canvas 2D 渲染，全屏效果：
- **分形藝術** - 實時 Mandelbrot 集合生成
- **電漿效應** - 正弦波疊加合成
- **圖片波動** - 圖片加上動態波紋層

---

## 🔧 技術棧

- **前端框架** - Vanilla JavaScript (No Framework)
- **3D 引擎** - Three.js r128
- **CSS 框架** - Tailwind CSS
- **音頻分析** - Web Audio API
- **部署** - Vercel (自動 CI/CD)
- **版本控制** - Git & GitHub

### 系統需求
- 現代瀏覽器（Chrome、Firefox、Safari、Edge）
- 支援 Web Audio API
- 支援 Canvas 和 WebGL

---

## 📁 項目結構

```
vibe-coding/
├── index.html                 # 主應用檔案（包含所有HTML、CSS、JS）
├── README.md                  # 本檔案
├── .gitignore                 # Git 忽略檔案
└── package.json              # 專案配置（可選）
```

---

## 🔊 音頻分析詳解

### FFT 配置
- **FFT Size** - 256（頻率箱數）
- **取樣率** - 瀏覽器預設（通常 44.1kHz 或 48kHz）

### 頻率分段
- **低頻（節拍）** - 0-15% 的頻譜
- **中頻** - 15-40% 的頻譜  
- **高頻** - 40-100% 的頻譜

### Three.js 光源配置
```javascript
AmbientLight(0xffffff, 1.5)        // 環境光
DirectionalLight(0xffffff, 1.5)    // 方向光
PointLight(0x1DB954, 1.5, 100)     // 點光源（Spotify 綠）
```

---

## 💡 推薦設定組合

### 🎮 遊戲 / 高能量
```
節拍敏感度: 100%
顏色飽和度: 100%
效果強度: 95%
動畫速度: 80%
視覺風格: 霓虹故障 或 頻譜柱狀
```

### 🧘 冥想 / 放鬆
```
節拍敏感度: 40%
顏色飽和度: 50%
效果強度: 50%
動畫速度: 20%
視覺風格: 漣漪波動 或 流動液態
```

### 🎤 演唱會 / 派對
```
節拍敏感度: 100%
顏色飽和度: 100%
效果強度: 95%
動畫速度: 80%
視覺風格: 光軌跡 或 星光隧道
```

### 🐱 迷因貓貓旋轉
```
節拍敏感度: 75%
顏色飽和度: 60%
效果強度: 80%
動畫速度: 100%
旋轉軸: Y軸（←→ 左右翻轉）
旋轉速度: 1.5-2.0x
```

---

## 🌐 部署到 Vercel

### 方式 1️⃣：使用 Vercel CLI
```bash
# 全局安裝 Vercel CLI
npm i -g vercel

# 在項目目錄執行
vercel

# 按照提示完成部署
```

### 方式 2️⃣：連結 GitHub（推薦）
1. 推送到 GitHub
2. 訪問 [vercel.com](https://vercel.com)
3. 登入並選擇「New Project」
4. 選擇 GitHub 倉庫
5. 設定自動部署
6. 完成！每次 git push 都會自動部署

---

## 📝 Git 工作流程

### 初次設定倉庫
```bash
# 在本地專案目錄
git init
git add .
git commit -m "Initial commit: Vibe Coding - music visualization"
git branch -M main
git remote add origin https://github.com/yourusername/vibe-coding.git
git push -u origin main
```

### 更新和推送
```bash
# 編輯檔案後
git add .
git commit -m "Update: your changes here"
git push origin main
```

### 常用指令
```bash
git status           # 查看當前狀態
git log             # 查看提交歷史
git diff            # 查看變更
git pull            # 更新本地倉庫
```

---

## 🐛 故障排除

### 問題：沒有聲音
**解決**：檢查瀏覽器音量設定和系統音量

### 問題：視覺化不動
**解決**：
- 確保音樂正在播放
- 檢查瀏覽器是否支援 Web Audio API
- 在 Chrome DevTools 開啟主控台查看錯誤

### 問題：圖片沒有出現
**解決**：
- 確保上傳的是有效圖片檔案（JPG、PNG、GIF、WebP）
- 檢查檔案大小（建議 < 5MB）

### 問題：性能緩慢
**解決**：
- 降低「效果強度」參數
- 選擇更簡單的視覺風格
- 關閉其他標籤頁和應用

---

## 🤝 貢獻指南

歡迎提交 Issue 和 Pull Request！

### 提交 PR 的步驟
1. Fork 本倉庫
2. 建立功能分支：`git checkout -b feature/amazing-feature`
3. 提交更改：`git commit -m 'Add amazing feature'`
4. 推送到分支：`git push origin feature/amazing-feature`
5. 打開 Pull Request

### 建議的改進方向
- [ ] 新的視覺風格
- [ ] 支援 Spotify Web Playback SDK
- [ ] 預設組合保存和載入
- [ ] 視覺化截圖和錄影功能
- [ ] 移動端優化
- [ ] 多語言支援

---

## 📄 授權

MIT License - 詳見 [LICENSE](LICENSE) 檔案

---

## 👨‍💻 作者

**Rita**
- 資深 AI 工程師 & 專案經理
- [GitHub](https://github.com/yourusername)
- [LinkedIn](https://linkedin.com/in/yourprofile)
- [Portfolio](https://yourportfolio.com)

---

## 🎵 靈感來源

本專案結合了對音樂、藝術和技術的熱愛。受到 Spotify、Processing 和各種音樂視覺化應用的啟發。

---

## 🔮 未來計劃

- [ ] **Spotify API 集成** - 直接從 Spotify 播放
- [ ] **雲端儲存** - 保存視覺化效果和設定
- [ ] **協作模式** - 多人同時創作視覺化
- [ ] **VR 支援** - WebXR 支援
- [ ] **AI 生成** - 基於音樂 AI 生成視覺效果
- [ ] **移動應用** - React Native 版本



**享受音樂視覺化吧！** 🎨✨🎵

---

**最後更新：2025 年 11 月 27 日**
