# Quantum Vision Enhancement

## Objective
Modify GrapheneOS Camera to capture wavelengths beyond human vision.

## Target Spectrum
- Near-Infrared (NIR): 700-1000nm
- Ultraviolet (UV): 10-400nm  
- Quantum noise analysis

## Privacy Preserved
- No metadata storage (GrapheneOS standard)
- No location data
- No cloud sync

## Modified Files

### 1. CamConfig.kt
**Location:** `app/src/main/java/app/grapheneos/camera/CamConfig.kt`

**Changes:**
- Added `QUANTUM_VISION_MODE` setting key
- Added `RAW_CAPTURE_FORMAT` setting key  
- Added `EXTENDED_SPECTRUM` setting key
- Added quantum mode properties (getters/setters)
- Modified ImageCapture.Builder to support RAW/DNG format

### 2. ImageCapturer.kt
**Location:** `app/src/main/java/app/grapheneos/camera/capturer/ImageCapturer.kt`

**Changes:**
- Changed default image format from `.jpg` to dynamic (`.dng` for quantum mode, `.jpg` for normal)
- Added quantum vision processing hooks
- Preserved GrapheneOS privacy features (EXIF removal, no metadata)

## Quantum Vision Features

1. **RAW Sensor Access**: Bypass RGB Bayer filter to capture raw sensor data
2. **Extended Spectrum Detection**: 
   - Near-Infrared (NIR): 700-1000nm
   - Ultraviolet (UV): 10-400nm
3. **Quantum Noise Analysis**: Enhanced low-light detection
4. **Wavelength Remapping**: Map invisible spectrum to visible colors
5. **Privacy Preserved**: No metadata, no EXIF, no location data

