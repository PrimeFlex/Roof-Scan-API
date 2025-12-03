# Roof Scan API (AI-Powered Roof Detection)

## Overview
Roof Scan API is an AI-powered detection service designed to analyze roof images and identify potential damage. Built for the PrimeFlex claims system, this tool helps adjusters, contractors, and homeowners quickly assess roof conditions before filing or pursuing a property claim.

The API processes images and detects:
- Missing shingles  
- Hail impact patterns  
- Wind damage markers  
- Tree impact zones  
- Soft spots, discoloration, or visible structural issues  

It’s designed to support fast pre-claim evaluations and improve the accuracy of on-site inspections.

---

## Features

### ✔ AI Image Analysis  
Processes roof photos and returns detected damage regions or classifications.

### ✔ Multiple Damage Types  
Identifies and labels common categories:
- Hail bruising  
- Wind-creased shingles  
- Missing tabs  
- Flashing issues  
- Granule loss  
- Debris impact marks  

### ✔ API Ready  
Structured to be used by:
- Web apps  
- Mobile apps  
- PrimeFlex Claims Assistant  
- Contractor dashboards  

### ✔ Fast Pre-Inspection Screening  
Gives users a quick “first pass” assessment before sending an adjuster or contractor.

---

## Possible Tech Stack (depending on implementation stage)

If the project uses AI models:

- **Python**
- **FastAPI or Flask**  
- **YOLOv8 / YOLOv9** for image detection *(or another vision model)*  
- **Roboflow** for dataset training  
- **OpenAI Vision API (optional)**  
- **NumPy / Pillow** for image handling  

If early-stage and still being built, just include:

> *Architecture currently in development; early prototype supports image upload and analysis workflow.*

---

## API Endpoints (Example)


**Body:**  
- `image`: Roof photo (JPEG/PNG)

**Response example:**
```json
{
  "status": "success",
  "damage_detected": true,
  "findings": [
    { "type": "missing_shingle", "confidence": 0.91 },
    { "type": "hail_impact", "confidence": 0.87 }
  ],
  "recommendation": "Inspection recommended. Visible signs of damage detected."
}


---

How It Works

User uploads a roof photo (drone, ladder shot, or ground-level zoom).

The API runs the image through a detection model.

Damage categories are classified and scored.

A structured JSON response is returned with:

detected damage

confidence levels

optional bounding-box data

high-level recommendation

Use Cases

Public adjusters performing early claim screening

Contractors giving post-inspection reports

Homeowners checking storm damage

AI assistants inside PrimeFlex tools

Drone-photo workflows for roof inspections

Future Enhancements

Bounding-box visualization for detected damage

Integrate OpenAI Vision API for secondary analysis

Support for infrared roof imaging

Add condition scoring (0–100 health rating)

Automated PDF summary reports

Direct integration with PrimeFlex Claims CRM

Author

Jeremy Perry
PrimeFlex Adjusters — Building practical AI to support property claims.

License

MIT License
