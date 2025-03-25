# 📡 TP 06: Frequency Filtering in Image Processing  

## 🎯 Objectives  
1. Understand the **2D Fourier Transform** applied to images.  
2. Visualize the **magnitude** and **phase** spectra of an image.  
3. Apply **frequency domain filters** (Low-pass, High-pass, and Notch filters) to enhance or analyze an image.  

---

## 📝 Steps  

### 🔹 1. Load & Display the Image  
- Load a **grayscale image** (e.g., `cameraman.tif`).  
- Load an image with **periodic noise** (e.g., `image_bruitee_Periodique.jpg`).  
- Display the images and their characteristics.  

---

### 🔹 2. Compute & Visualize the Frequency Spectrum  
- Compute the **2D Fourier Transform** (`fft2`).  
- Shift the frequency domain representation to center the **low frequencies** (`fftshift`).  
- Display:  
  - **Magnitude Spectrum**  
  - **Phase Spectrum**  

---

### 🔹 3. Low-Pass Filtering  
- Create an **Ideal Low-Pass Filter**.  
- Apply the filter to the frequency spectrum.  
- Observe the effect on the **reconstructed image**.  

```python
# Example of low-pass filtering
filtered_F = Fshift * mask_lowpass
image_filtered = np.fft.ifft2(np.fft.ifftshift(filtered_F))
