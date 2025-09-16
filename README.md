"# Agricultural-Field-Monitoring-with-Drone-Images" 
🌾 Agri-Field Monitoring with Drone Images

This project is a drone-based agricultural field monitoring system that analyzes aerial images of farmland. It detects red-marked boundaries, extracts the crop field area, identifies navigable paths, and generates overlays and statistical reports for better farm management.

🚀 Features

Drone Image Upload: Upload high-resolution aerial/drone images of farmlands.

Boundary Detection: Detects red-marked field boundaries using HSV and LAB color filtering.

Field Segmentation: Extracts the crop field area based on detected boundaries.

Path Detection: Identifies paths between crops for navigation and monitoring.

Smart Visualization:

🟥 Red = Field boundaries

🟩 Green = Crop field area

🟦 Blue = Paths inside the field

Analysis & Reporting:

Field coverage %

Boundary detection quality

Path density statistics

Interactive Tuning: Adjust sensitivity for red boundary detection.

Export Results: Save processed images and analytical reports.

📦 Installation

Run in Google Colab:

!pip install scikit-image opencv-python matplotlib pillow

🛠️ Workflow

Upload Drone Image

original_image = upload_image()


(Ensure the field boundary is marked in red in your drone image)

Detect Boundaries & Field Area

field_mask, red_lines, field_pixels, field_percentage = detect_field_area_with_red_boundary(original_image)


Path Detection

path_binary, path_skeleton = detect_paths_in_field(original_image, field_mask, red_lines)


Overlay Visualization

display_red_boundary_analysis()


✅ Shows original drone image, detected boundary, field area, paths, and overlays.

Generate Statistical Report

print_red_boundary_analysis_summary()


Interactive Fine-Tuning (optional)

interactive_red_detection_tuning()


Save Results

save_analysis_results()

📊 Example Outputs

Drone Image with Red Boundary Detection

Crop Field Segmentation (Green Mask)

Path Skeleton Overlay (Blue)

Final Enhanced Overlay (Red + Green + Blue)

Statistical Report

📂 Notebook Structure

Cell 1 → Install dependencies

Cell 2 → Import libraries

Cell 3 → Upload drone image

Cell 4–5 → Boundary + Field detection

Cell 6 → Path detection

Cell 7 → Red boundary analysis

Cell 8 → Overlay visualization

Cell 9 → Full results display

Cell 10 → Statistical report

Cell 11 → Interactive tuning

Cell 12 → Save final results

⚠️ Requirements & Assumptions

Input drone images must have red boundaries clearly marked.

Works best with high-resolution aerial drone footage.

Detection quality depends on lighting, contrast, and red boundary visibility.

✅ Future Scope

AI-based automatic crop health detection.

Multi-spectral drone image support (NDVI, thermal).

GPS integration for geo-referenced field monitoring.

Real-time monitoring dashboard for farmers.