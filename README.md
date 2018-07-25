# AutoEQ

### Todo
- Custom compensation curve based on Serious and brighter tilt
- Separate results by source and tuning
- README in batch result directory with parameters

### Documentation
  - Results
    - Links to sources
    - Usage with HeSuVi
    - Parameters used
  - In ear data, everything in CSV, compensations, calibrations
  - Installing
    - python3
    - pip3
    - Virtualenv
    - requirements.txt
  - https://apps.automeris.io/wpd/
  - frequency_response.py
    - CLI args
    - Examples
    - Use cases
  - General
    - Smoothing
    - Interpolating
    - Max gain with smoothed corners
  - Compensation
    - Curve to turn raw microphone data into error data
    - Targets have no bass boost
    - Innerfidelity 2016
    - Innerfidelity 2017 (link to post)
    - Innerfidelity SBAF-Serious (how was made)
    - Headphone.com (how was made)
  - Equalizing to other headphones
  - Calibration (raw - calibration data)
    - Same headphone models selected from both
    - Difference in error calculated. Errors obtained by respective compensation curves.
    - Calibration data is to be subtracted from error data (compensated data)
    - Calibrating raw microphone data makes no sense because systems are different
  - Data processing
    - Not meant as a user friendly tool. Obtaining data needs to be done only once.
    - Innerfidelity
      - Innerfidelity PDFs crawled. PDFs turned into images. Images turned into data. All inspected manually.
      - Read data is the red and blue curves which are compensated with old compensation curve
      - Compensation curve 2016 obtained from Innerfidelity image
      - Compensation curve 2017 obtained from Innerfidelity image (see article...)
      - Transformation curve made from compensation curves
      - Data turned into raw data by adding compensation curve 2016
      - Original data still saved
    - Headphone.com
      - Raw data images crawled. Compensated data images crawled. Images turned into data. All inspected manually.
      - Raw and compensated data used to produce compensation curve.
      - Only raw data kept.
