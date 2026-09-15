# OilTrace: Automated Marine Oil Spill Detection & AIS Attribution Engine (SIH26143)

## System Overview
OilTrace is an evidence-driven pipeline developed for SIH 2026 (Problem Statement ID: SIH26143 by NTRO). 
It combines C-band Sentinel-1 SAR imagery, metocean drift modeling (HYCOM/ERA5), and high-throughput AIS trajectory analytics to reconstruct spill origin corridors and rank suspect vessels.

## Project Structure
├── sar_processing/     # Preprocessing (SNAP/GDAL) & U-Net Segmentation
├── drift_modeling/     # OpenDrift / OpenOil Lagrangian particle back-tracking
├── ais_engine/         # High-speed Parquet/Polars/DuckDB ingestion & track builder
├── attribution/        # Transparent Candidate Scoring & AIS gap analysis
└── dashboard/          # MapLibre GL & FastAPI investigator interface


## Tech Stack
- **AI/ML:** PyTorch, U-Net (ResNet-34 backbone)
- **Drift Simulation:** OpenDrift / OpenOil Framework
- **AIS Analytics:** Python, Polars, DuckDB, Apache Parquet
- **GIS Backend:** PostGIS, GDAL, Rasterio
- **Frontend:** Next.js, MapLibre GL, Tailwind CSS
