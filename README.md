# Debug Image Viewer (former OpenCV Image Viewer) Plugin

*This is a repository for reporting bugs and asking questions related to the [Debug Image Viewer (former OpenCV Image Viewer)](https://plugins.jetbrains.com/plugin/14371-opencv-image-viewer) plugin.*

## Description

**Numpy | OpenCV | Pillow | PyTorch | TensorFlow** 

The plugin displays an image without stopping the debugger. The basic (free) version allows working on OpenCV Images (ndarray or Mat). The premium version also supports Pillow/PIL images, and Tensorflow and PyTorch tensors. This will enable you to observe the data you are currently working on.

There are three ways to display the image/tensor during debugging:
- **middle-click** (middle mouse button);
- a keyboard shortcut **Alt+I** (default keymap);
- an action from the **context menu** of the variable.

The Debug Image Viewer is a multifunctional tool that displays data in three modes: [**popup, dialog or tool window**](https://plugins.jetbrains.com/plugin/14371-opencv-image-viewer/features). Change this option in the settings and see which mode is right for you. The plugin allows you to display the variable name, image size, color depth, and data type. In addition to displaying the image, Debug Image Viewer also allows [**inverting BGR into RGB channels**](https://plugins.jetbrains.com/plugin/14371-opencv-image-viewer/features) and [**saving the image**](https://plugins.jetbrains.com/plugin/14371-opencv-image-viewer/features) in PNG format. 

Grayscale, BGR, or BGRA images are supported by default. Also, multichannel arrays can be viewed, for which [**each channel is displayed separately**](https://plugins.jetbrains.com/plugin/14371-opencv-image-viewer/features). You can also [**apply a colormap**](https://plugins.jetbrains.com/plugin/14371-opencv-image-viewer/features) to any single channel.

One of the most important plugin options is [**normalization**](https://plugins.jetbrains.com/plugin/14371-opencv-image-viewer/features). That is the procedure that modifies the pixel values' scale. Normalization aims to bring an image to a range that is normal to sense. Normalization is a very useful technique when working with data science since it enables displaying matrices beyond the typical image range.

The displaying behavior:
- If the array is `uint8` or `quint8`, it is **displayed as is**;
- If the array is `int8` or `qint8`, the pixel values are added to 128 (`[-128,127] -> [0,255]`);
- If the array is `uint16`, `uint32`, `uint64` or `quint16`, the pixel values are divided by 256 (`[0,65280] -> [0,255]`);
- If the array is `int16`, `int32`, `int64`, `qint16` or `qint32`, the pixel values are divided by 256 then added to 128 (`[-32768,32512] -> [0,255]`);
- If the array is `float16`, `float32`, `float64` or `bloat16`, the pixel values are multiplied by 255 (`[0,1] -> [0,255]`);
- If the array is `boolean`, the pixel values are multiplied by 255 (`{False,True} -> {0,255}`).

To work with Debug Image Viewer, the image must be in **HWC** or **CHW** format when you use Python. For the C++ environment, the image must be a **contiguous** array.

Debug Image Viewer provides a simple and **user-friendly interface** for displaying images which makes work much easier. The plugin is a tool for developers and researchers working with OpenCV, Pillow/PIL, TensorFlow, or PyTorch, as it provides an efficient and intuitive way to **view and analyze image data**.

Debug Image Viewer is a graphical user interface (GUI) plugin for JetBrains IDEs that allows users to easily display OpenCV and PIL images, Tensorflow and PyTorch tensors during debugging. Only OpenCV visualization is available in the free version. You can check all the features below.

![](https://plugins.jetbrains.com/files/14371/34520-page/56a6eb0c-3cf0-47f1-b5f8-c644e92912d2)

**Feature not yet available. We are working on the implementation. All available features are listed below.*

## Free

- the ability to **change the window mode**: popup or dialog:
    - light popup disappears when un-clicked; 
    - dialog remains visible until you close it; allows you to display (unlike a popup) several images at once;

![](https://plugins.jetbrains.com/files/14371/2032-page/bce1aac9-1f57-426e-bcef-653733d0398a)

- displaying the **cursor position and pixel value** under the cursor;

![](https://plugins.jetbrains.com/files/14371/2032-page/25d03827-4973-4c9a-8897-1c7b2b0354f5)

- possibility to **copy the image** to external programs (e.g., GIMP) and **save the image to disk**;

![](https://plugins.jetbrains.com/files/14371/2032-page/72c6e071-f10d-4eb9-a1d0-0efb156a38e9)

- **remembering the position** of the last opened picture and opening another one in the same place;

![](https://plugins.jetbrains.com/files/14371/2032-page/6e63ac6c-7ec5-4826-ade3-a17874fd9bcd)

- **remembering the size** of the last opened picture and opening another one in the same size;

![](https://plugins.jetbrains.com/files/14371/2032-page/209af9c3-8ac7-47b4-9cd6-856f8bbedc18)

- **force “view as image”** (C++ only) for other types containing Mat e.g. std::shared_ptr<Mat>;

![](https://plugins.jetbrains.com/files/14371/2032-page/61a2f638-f6de-4cd2-86eb-21b650a867e4)

- displaying the image **directly from the editor**;

![](https://plugins.jetbrains.com/files/14371/2032-page/fb36c435-d73d-49b9-889d-03a78f539ee2)

- **startup notifications**: contains info about changes in the new version.

![](https://plugins.jetbrains.com/files/14371/2032-page/7c7ab092-5656-4f74-82fe-fc77b011c302)

## Premium

- **channel inversion**: from BGR to RGB and RGB to BGR;

![](https://plugins.jetbrains.com/files/14371/2032-page/eb285c21-db6a-4bb5-8fe5-70d99b1918ff)

- **normalization** of the image: stretching the range of values to an interval appropriately defined for the type of the variable;

![](https://plugins.jetbrains.com/files/14371/2032-page/ea243ddc-4346-41c3-90b3-94462e494e8d)

- **image transposition** from HWC to CHW and vice versa;

![](https://plugins.jetbrains.com/files/14371/2032-page/056b3b73-57a8-4562-915a-265df9fb60d7)

- **displaying channels separately** as single-channel images;

![](https://plugins.jetbrains.com/files/14371/2032-page/f959e3af-d0e1-4e2a-a145-4cd18838af37)

- **applying a pseudo-color** to a single-channel image;

![](https://plugins.jetbrains.com/files/14371/2032-page/65d4d0d2-2080-43d1-a902-8f4d5dfe621f)

- **displaying the pixel value in hexadecimal** under the cursor;

![](https://plugins.jetbrains.com/files/14371/2032-page/9529dc3f-1c5e-440e-a767-81d69797f22a)

- support for **batch dimension BxHxWxC**;

![](https://plugins.jetbrains.com/files/14371/2032-page/bf1c8685-7d40-44d2-af65-0e1d9905315d)

- displaying **multiple images**.

![](https://plugins.jetbrains.com/files/14371/2032-page/6af3dc8c-276f-4f05-80f7-70abac13dea0)

## Language support

Debug Image Viewer plugin brings full support for the following languages: **Python, C++, Java/Kotlin/Android**. 

*Note it may work for other languages, but they are not officially supported or tested for now.*

### Python - there are several modes in which you can display the image
- variable type: numpy (ndarray), Pillow/PIL* (Image, ImageFile), PyTorch* (Tensor, Parameter), TensorFlow* (EagerTensor, ResourceVariable)
- data type: bool, uint8, uint16, uint32, uint64, int8, int16, int32, int64, float16, bfloat16, float32, float64, quint8, quint16, qint8, qint16, qint32
- number of dimensions:
    - 1D: any
    - 2D: any
    - 3D: any*
    - 4D: any*
    - 5D and more*: any if first dimensions are ones (e.g. 1x1x2x100x100x3) 

**Premium version only*

* debug mode 

![](https://plugins.jetbrains.com/files/14371/2032-page/28cf7e4e-d63f-4970-8211-f9d400f1da9c)

* console mode

![](https://plugins.jetbrains.com/files/14371/2032-page/c7e62c2d-7195-45b7-aabf-93808bff3bf5)

*  jupyter notebook mode

![](https://plugins.jetbrains.com/files/14371/2032-page/ab25b441-a67a-4964-8bae-b99886b941ff)

* remote interpreter

![](https://plugins.jetbrains.com/files/14371/2032-page/e1ead006-88ca-450e-a988-1e0174b38a45)

### C++
- variable type: Mat, Mat\*, Mat\*\* Mat&, Mat&&, const Mat, const Mat\*, const Mat&, const Mat&& [1]
- data type: CV_8U, CV_16U, CV_8S, CV_16S, CV_32S, CV_32F, CV_64F
- number of dimensions:
    - 3D: any height, any width, 1, 3, or 4 channels
    - 4D: any batch, any height, any width, 1, 3, or 4 channels

*[1] Force View As Image for other types containing Mat available*

![](https://plugins.jetbrains.com/files/14371/2032-page/e9a99b9b-df5d-4fc0-b5ae-e124b517a726)

### Java/Kotlin
- variable type: Mat
- data type: CV_8U, CV_16U, CV_8S, CV_16S, CV_32S, CV_32F, CV_64F
- number of dimensions:
    - 2D: any
    - 3D: any height, any width, 1, 3, or 4 channels
    - 4D: any batch, any height, any width, 1, 3, or 4 channels

![](https://plugins.jetbrains.com/files/14371/2032-page/0ee50533-3cdc-4e27-8b82-a3e344d3626d)

### Android
- variable type: Mat
- data type: CV_8U, CV_16U, CV_8S, CV_16S, CV_32S, CV_32F, CV_64F
- number of dimensions:
    - 2D: any
    - 3D: any height, any width, 1, 3, or 4 channels
    - 4D: any batch, any height, any width, 1, 3, or 4 channels

![](https://plugins.jetbrains.com/files/14371/2032-page/d446799b-5116-49f2-8c96-2e52366bec17)

### Summary

![](https://plugins.jetbrains.com/files/14371/2032-page/a97c982d-5772-481e-b8ef-297faa844c61)

*[1] Force View As Image for other types containing Mat available*
