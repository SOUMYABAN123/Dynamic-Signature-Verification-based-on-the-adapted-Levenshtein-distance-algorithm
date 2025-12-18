# Dynamic-Signature-Verification-based-on-the-adapted-Levenshtein-distance-algorithm
The aim of this experiment is to design, implement, and evaluate a dynamic (online) signature verification system based on a string-based representation of signature dynamics and an adapted Levenshtein (minimum edit) distance algorithm

# Aim of Experiment:
The aim of this experiment is to design, implement, and evaluate a dynamic (online) signature verification system based on a string-based representation of signature dynamics and an adapted Levenshtein (minimum edit) distance algorithm, as described in Chapter 6 of the Image Processing.
More specifically, the experiment seeks to:
•	Convert raw online signature data, captured as time-ordered coordinate sequences, into a symbolic string representation that preserves the essential dynamic characteristics of handwriting.
•	Apply an adapted and normalized Levenshtein distance to measure the similarity between reference and test signatures, accounting for natural intra-user variations in signing behaviour.
•	Investigate the effectiveness of string-based matching for distinguishing genuine signatures from forgeries in a dynamic verification setting.
•	Demonstrate that techniques from string processing and edit-distance theory can be successfully integrated into image processing and biometric verification tasks.
Overall, the experiment aims to validate that a string-based, edit-distance-driven approach provides a robust and interpretable method for dynamic signature verification.

# Flow chart of the project:
<img width="505" height="758" alt="image" src="https://github.com/user-attachments/assets/e856171f-4f63-4db3-81df-b19e4082dafb" />

# Mathemetical intuition:
<img width="851" height="443" alt="image" src="https://github.com/user-attachments/assets/7a474433-e4bd-4be4-a49a-8c96fbde8374" />
<img width="850" height="197" alt="image" src="https://github.com/user-attachments/assets/bac461ac-1f9b-4bd2-b712-147a102ac384" />
<img width="897" height="316" alt="image" src="https://github.com/user-attachments/assets/526e7294-63df-42c0-9874-38a9810b5c99" />
<img width="852" height="242" alt="image" src="https://github.com/user-attachments/assets/af4e863b-0006-4f29-8304-45fd9fd2f2a3" />
<img width="831" height="163" alt="image" src="https://github.com/user-attachments/assets/8cd219f5-ffce-49a1-b7e8-0854920f3921" />

# Concept summary:
Algorithm / Model Used: Adapted Levenshtein distance algorithm
Input: The input dataset used in this project consists of online (dynamic) signature samples, where each signature is recorded as a time-ordered sequence of points rather than a static image.
Each signature sample typically includes the following attributes per time step:
	x-coordinate of the pen position
	y-coordinate of the pen position
	Time index / sample order
	Pen status (pen-down / pen-up), used to segment strokes
Optionally, depending on the acquisition device, additional features such as pressure, azimuth, or altitude may be present, but the core algorithm relies on x, y, and pen status.

# Result analysis and Signature and stroke plots:
U3S40.TXT -
<img width="599" height="461" alt="image" src="https://github.com/user-attachments/assets/b5ef7e6a-0a00-414c-bc47-4f2ce0c32918" />
<img width="616" height="485" alt="image" src="https://github.com/user-attachments/assets/59ddc7e9-eddc-44ed-b30a-695f79afb115" />

US713.TXT-
<img width="572" height="445" alt="image" src="https://github.com/user-attachments/assets/951e84f9-2939-4e95-b50d-a249eb453ff7" />
<img width="576" height="447" alt="image" src="https://github.com/user-attachments/assets/1a0126ef-40f8-4ea9-a2ad-33c8779dc644" />

# Comparison of U7S13 against U3S40:
Normalized Levenshtein Distance: 0.5521
Verification Threshold: 0.3
Signature Accepted: False

# Comparision of U3S40 against U3S40:
Normalized Levenshtein Distance (self-comparison): 0.0
Verification Threshold: 0.1
Signature Accepted: True

# Conclusion and future scope:
This project successfully demonstrates a dynamic signature verification system based on a string-based representation of handwriting dynamics and an adapted Levenshtein distance algorithm, as described in Chapter 6 of the Image Processing lecture notes. By converting online signature trajectories into sequences of symbolic stroke-strings, the system effectively captures both local stroke dynamics and global signature structure.
The experimental results validate the correctness of the approach: preprocessing and stroke segmentation preserve the essential shape of the signature, while self-comparison yields a normalized Levenshtein distance of zero, confirming the reliability of the implementation. The use of normalization and threshold-based decision making enables consistent verification across signatures of varying lengths. Overall, the method provides a robust, interpretable, and computationally efficient solution for online signature verification.

Future Scope
The proposed system can be further extended and improved in several directions:

•	Enhanced feature encoding: Incorporating additional dynamic features such as pen pressure, velocity, or curvature could improve discrimination between genuine signatures and skilled forgeries.
•	Adaptive weighting: Learning edit-operation weights from data rather than fixing them manually may lead to better performance.
•	Threshold optimization: Thresholds can be user-specific or learned using statistical or machine-learning techniques.
•	Forgery evaluation: Testing the system on a larger dataset containing random and skilled forgeries would provide a more comprehensive performance assessment.
•	Hybrid approaches: Combining string-based distance measures with machine learning or deep learning models could further enhance verification accuracy.
•	
In summary, while the current system effectively validates the theoretical approach, these extensions offer clear pathways toward a more accurate and scalable real-world signature verification solution.















