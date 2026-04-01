# Data Dictionary

## FactJobs
| Column | Type | Description |
|--------|------|-------------|
| Job ID | Integer | Unique job identifier |
| Posting Date | Date | Date job was posted |
| Status | Text | Open or Closed |
| Region | Text | Geographic region |
| State | Text | State location |
| Sales Consultant | Text | Assigned recruitment consultant |
| Specialization | Text | Medical specialization category |
| Conversion Indicator | Integer | 1 = Closed, 0 = Open |

## DimDate
| Column | Type | Description |
|--------|------|-------------|
| Date | Date | Full date value |
| Month | Text | Month name |
| Year | Integer | Calendar year |
| Quarter | Text | Q1 through Q4 |

## DimConsultant
| Column | Type | Description |
|--------|------|-------------|
| Consultant ID | Integer | Unique identifier |
| Consultant Name | Text | Full name |

## DimSpecialization
| Column | Type | Description |
|--------|------|-------------|
| Specialization ID | Integer | Unique identifier |
| Specialization Name | Text | Medical specialization |

## DimRegion
| Column | Type | Description |
|--------|------|-------------|
| Region ID | Integer | Unique identifier |
| Region Name | Text | Geographic region |
| State | Text | State within region |
