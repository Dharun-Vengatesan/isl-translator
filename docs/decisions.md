# Architectural Decisions Log

## 2026-09-27 — MediaPipe API choice
Decision: Use `mediapipe.tasks.python.vision.HandLandmarker` (Tasks API), not the deprecated `mp.solutions.hands`.
Reason: Classic `solutions` API is no longer available in installable MediaPipe (confirmed: mediapipe 1.0.1, `mp.solutions` does not exist).
Impact: Requires downloading `hand_landmarker.task` model file (Stage 2). Output structure (landmarks, handedness, confidence) unchanged.