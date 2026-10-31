目标检测，数据集，排水管道缺陷【检测】数据集

共19049张图像，均为原图，未经过数据增强

按照我国规程CJJ181-2012标注了15类缺陷，1类不在规程里的缺陷【异物】，附加1类正常样本【管道接口】
因此，本数据集共17类样本

数据集包括图片和相应标注文件，有VOC数据集格式，文件后缀为.xml，可用于大部分模型训练。


根据您提供的信息，这里将排水管道缺陷检测数据集的相关信息整理成表格形式：

### **排水管道缺陷检测数据集统计**

| **项目** | **详情** |
| :--- | :--- |
| **总图像数** | 19,049 张 |
| **是否经过数据增强** | 否 |
| **标注依据** | CJJ181-2012 规程 |
| **类别总数** | 17 类 |

---

### **按类别统计**

| **类别名称** | **备注** |
| :--- | :--- |
| 破损 | 根据CJJ181-2012规程 |
| 变形 | 根据CJJ181-2012规程 |
| 腐蚀 | 根据CJJ181-2012规程 |
| 错口 | 根据CJJ181-2012规程 |
| 起伏 | 根据CJJ181-2012规程 |
| 脱节 | 根据CJJ181-2012规程 |
| 残墙、坝根 | 根据CJJ181-2012规程 |
| 结垢 | 根据CJJ181-2012规程 |
| 垢块 | 根据CJJ181-2012规程 |
| 异物 | 不在规程内的额外类别 |
| 正常样本（管道接口） | 附加的正常样本类别 |
| ... | 其他根据CJJ181-2012规程分类的缺陷类型（共15类加上异物和正常样本共17类） |

### **数据集格式**

| **格式** | **文件后缀** | **用途** |
| :--- | :--- | :--- |
| VOC 数据集格式 | .xml | 大部分模型训练 |

基于CJJ181-2012规程分类的具体缺陷类型未一一列出，但总共包括了15种按照规程定义的缺陷类型，加上不在规程里的“异物”缺陷和作为正常样本的“管道接口”，共计17种类别。

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7216046e799043a2a4f3ff10033ab86f.png)
1
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/db4658847c874dc6b0a793fe628b4a9d.png)
1
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d1d783f815b241fe848d38c35bab4945.png)
运维管理平台

：集成到市政设施管理系统中，实现数字化、智能化管理。


![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/bd0ed55432c94d96a9bcc951b8f05d34.jpeg)



![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b6c642542b964bc0bfe08361c3c4e1ce.jpeg)


![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7e4650f78f8d4c4e8e5a14fb04ec756c.jpeg)








  ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1e7fd1a23505491bb74191be6925959d.jpeg)


- 数据集详细表格说明  
- VOC 格式标注说明  
- **基于 YOLOv8 的详细训练代码（支持 VOC 转 YOLO）**  
- 推理与可视化代码  
- 模型评估建议  

---

## 📊 排水管道缺陷检测数据集概览（表格版）

### ✅ **数据集总体统计**

| 项目 | 详情 |
| :--- | :--- |
| **总图像数** | 19,049 张 |
| **是否数据增强** | 否（可训练时启用增强） |
| **标注标准** | 《城镇排水管道检测与评估技术规程》CJJ/T 181-2012 |
| **类别总数** | 17 类 |
| **标注格式** | VOC XML（`.xml`）为主，可转换为 YOLO 格式 |
| **适用任务** | 目标检测 / 实例分割（推荐目标检测） |
| **推荐模型** | **YOLOv8s / YOLOv8m**（兼顾小目标与多类别） |

---

### ✅ **17 类缺陷详细分类表**

| 类别 ID | 类别名称（中文） | 类别名称（英文/建议标签） | 是否符合 CJJ181-2012 | 备注 |
| :---: | :--- | :--- | :---: | :--- |
| 0 | 破损 | breakage | ✅ | 结构断裂或孔洞 |
| 1 | 变形 | deformation | ✅ | 管道截面形状改变 |
| 2 | 腐蚀 | corrosion | ✅ | 内壁材料化学劣化 |
| 3 | 错口 | misalignment | ✅ | 接口错位 |
| 4 | 起伏 | undulation | ✅ | 管道纵向不平 |
| 5 | 脱节 | dislocation | ✅ | 接口分离 |
| 6 | 残墙、坝根 | leftover_wall | ✅ | 施工遗留障碍物 |
| 7 | 结垢 | scaling | ✅ | 表面沉积物覆盖 |
| 8 | 垢块 | scale_chunk | ✅ | 大块沉积物脱落风险 |
| 9 | 异物 | foreign_object | ❌ | 非规程类，额外添加 |
| 10 | 正常样本（管道接口） | normal_joint | ❌ | 正常状态，用于对比学习 |
| 11~16 | 其他CJJ181-2012缺陷 | e.g. infiltration, crack, etc. | ✅ | 如：渗漏、裂缝、树根侵入等（具体名称需根据实际补充） |

> ⚠️ **说明**：实际使用中需确认其余 6 类缺陷的准确名称，并统一命名（建议使用英文小写 snake_case，如 `tree_root`, `infiltration`, `crack`, `collapse`, `joint_separation`, `sediment`）。

---

### ✅ **数据集格式说明**

| 格式 | 文件后缀 | 用途 | 是否支持直接训练 |
| :--- | :--- | :--- | :--- |
| **VOC XML** | `.xml` | 原始标注格式，含边界框与类别 | ❌ 不支持 YOLO 直接训练 |
| **YOLO TXT** | `.txt` | 每图一个文件，每行：`class_id x_center y_center w h`（归一化） | ✅ 支持 YOLOv8 训练 |
| **图像文件** | `.jpg`, `.png` | 管道内窥图像 | ✅ 所有模型通用 |

---

## 🔄 步骤1：VOC XML 转 YOLO TXT 脚本

```python
# voc_to_yolo.py
import os
import xml.etree.ElementTree as ET
from pathlib import Path

# ==================== 配置 ====================
# 请根据实际类别顺序填写（必须与 data.yaml 一致）
class_names = [
    'breakage', 'deformation', 'corrosion', 'misalignment',
    'undulation', 'dislocation', 'leftover_wall', 'scaling',
    'scale_chunk', 'foreign_object', 'normal_joint',
    'infiltration', 'crack', 'tree_root', 'collapse', 'sediment', 'joint_separation'
]

class_to_id = {name: i for i, name in enumerate(class_names)}
voc_dir = "pipeline_dataset/annotations"  # VOC XML 所在目录
yolo_label_dir = "pipeline_dataset/labels/train"  # 输出目录
img_width = 640  # 假设训练分辨率，也可从图像读取
img_height = 640

os.makedirs(yolo_label_dir, exist_ok=True)

def convert_xml_to_yolo(xml_file):
    tree = ET.parse(xml_file)
    root = tree.getroot()
    yolo_lines = []

    for obj in root.findall('object'):
        cls_name = obj.find('name').text.strip().lower()
        # 统一命名（可加映射表）
        if cls_name in ['残墙', '坝根']:
            cls_name = 'leftover_wall'
        elif cls_name == '正常样本':
            cls_name = 'normal_joint'
        # 其他映射可在此添加

        if cls_name not in class_to_id:
            print(f"⚠️ 跳过未知类别: {cls_name}")
            continue

        cls_id = class_to_id[cls_name]
        bbox = obj.find('bndbox')
        xmin = float(bbox.find('xmin').text)
        ymin = float(bbox.find('ymin').text)
        xmax = float(bbox.find('xmax').text)
        ymax = float(bbox.find('ymax').text)

        # 归一化
        x_center = ((xmin + xmax) / 2) / img_width
        y_center = ((ymin + ymax) / 2) / img_height
        width = (xmax - xmin) / img_width
        height = (ymax - ymin) / img_height

        yolo_lines.append(f"{cls_id} {x_center:.6f} {y_center:.6f} {width:.6f} {height:.6f}")

    # 保存 .txt
    txt_file = Path(yolo_label_dir) / (Path(xml_file).stem + ".txt")
    with open(txt_file, "w") as f:
        f.write("\n".join(yolo_lines))

# 批量转换
for xml_file in Path(voc_dir).glob("*.xml"):
    convert_xml_to_yolo(xml_file)

print("✅ VOC → YOLO 转换完成！")
```

---

## 📄 `data.yaml` 配置文件

```yaml
# data.yaml
train: ./pipeline_dataset/images/train
val: ./pipeline_dataset/images/val
test: ./pipeline_dataset/images/test

# 类别数量
nc: 17

# 类别名称（必须与转换脚本一致）
names: [
  'breakage', 'deformation', 'corrosion', 'misalignment',
  'undulation', 'dislocation', 'leftover_wall', 'scaling',
  'scale_chunk', 'foreign_object', 'normal_joint',
  'infiltration', 'crack', 'tree_root', 'collapse', 'sediment', 'joint_separation'
]
```

---

## 🚀 YOLOv8 详细训练代码

```python
# train_pipeline.py
from ultralytics import YOLO
import torch
import os

# ==================== 配置 ====================
MODEL_TYPE = 'yolov8m.pt'           # 推荐：v8m 或 v8l（多类别）
DATA_CONFIG = 'pipeline_dataset/data.yaml'
EPOCHS = 200
BATCH_SIZE = 16
IMG_SIZE = 640
PROJECT_NAME = 'pipeline_defect_detection'
EXPERIMENT_NAME = 'yolov8m_640_pipe'

os.makedirs(f"runs/train/{EXPERIMENT_NAME}", exist_ok=True)

# ==================== 设备检查 ====================
DEVICE = '0' if torch.cuda.is_available() else 'cpu'
print(f"✅ 使用设备: {DEVICE}")

# ==================== 加载模型 ====================
model = YOLO(MODEL_TYPE)

# ==================== 开始训练 ====================
results = model.train(
    data=DATA_CONFIG,
    epochs=EPOCHS,
    batch=BATCH_SIZE,
    imgsz=IMG_SIZE,
    project=PROJECT_NAME,
    name=EXPERIMENT_NAME,
    save=True,
    save_period=10,
    device=DEVICE,
    workers=4,
    optimizer='AdamW',
    lr0=1e-3,
    lrf=1e-2,
    momentum=0.937,
    weight_decay=1e-4,
    warmup_epochs=3.0,
    box=7.5,
    cls=0.5,
    dfl=1.5,
    close_mosaic=15,
    augment=True,
    hsv_h=0.015,
    hsv_s=0.7,
    hsv_v=0.4,
    degrees=10.0,
    translate=0.2,
    scale=0.5,
    shear=2.0,
    flipud=0.0,
    fliplr=0.5,
    mosaic=1.0,
    mixup=0.1,
    copy_paste=0.1,  # 对小缺陷（如裂纹）有效
    patience=50,     # 早停
)

print("🎉 训练完成！")
print(f"📌 模型保存路径: runs/train/{EXPERIMENT_NAME}")
```

---

## 🔍 验证与评估

```python
# validate.py
from ultralytics import YOLO

model = YOLO(f'runs/train/{EXPERIMENT_NAME}/weights/best.pt')
metrics = model.val(
    data='pipeline_dataset/data.yaml',
    split='val',
    imgsz=640,
    batch=16,
    device=0 if torch.cuda.is_available() else 'cpu',
    save_json=True,
    conf=0.001,
)

print(f"📊 mAP@0.5: {metrics.box.map:.4f}")
print(f"📊 mAP@0.5:0.95: {metrics.box.map50:.4f}")
print(f"📊 Precision: {metrics.box.p:.4f}")
print(f"📊 Recall: {metrics.box.r:.4f}")

# 按类别输出 AP
for i, name in enumerate(class_names):
    print(f"  ├─ {name}: AP@0.5 = {metrics.box.ap[i]:.4f}")
```

---

## 🔦 推理代码（支持单图/视频/目录）

```python
# predict.py
from ultralytics import YOLO

model = YOLO('runs/train/yolov8m_640_pipe/weights/best.pt')
source = 'pipeline_dataset/images/test'  # 图像/视频/目录

results = model.predict(
    source=source,
    imgsz=640,
    conf=0.3,
    iou=0.5,
    device=0 if torch.cuda.is_available() else 'cpu',
    show=False,
    save=True,
    project='runs/predict',
    name='pipeline_result',
    line_width=2,
    verbose=True
)

for r in results:
    boxes = r.boxes
    print(f"🖼️ {r.path}:")
    for box in boxes:
        cls_id = int(box.cls[0])
        conf = float(box.conf[0])
        label = model.names[cls_id]
        print(f"  ├─ {label}: {conf:.2f}")
```

---

![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c3d2a5f7a90a4685beb8a5a8245280c9.png)

