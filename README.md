# N-Bit Digital Modulation Simulator

A scalable digital modulation simulator built with LabVIEW supporting:

- ASK
- PSK
- FSK
- QAM

with configurable **N bits per symbol**.

The project dynamically generates:
- modulated waveforms
- symbol mapping
- QAM constellation diagrams

using Formula Nodes to simplify modulation logic.

---

## Features

- Configurable N-bit per symbol modulation
- Supports:
  - M-ASK
  - M-PSK
  - M-FSK
  - M-QAM
- Automatic symbol extraction from binary input
- Binary-to-decimal symbol conversion
- Dynamic waveform generation
- QAM constellation visualization
- Scalable architecture

### M-ary Relation

```math
M = 2^N
```

Examples:
- N = 1 → Binary modulation
- N = 2 → 4-PSK / 4-QAM
- N = 4 → 16-QAM
- N = 6 → 64-QAM

---

## Project Structure

```text
Binary Input
      ↓
N-bit Symbol Extraction
      ↓
Binary → Decimal Conversion
      ↓
Modulation Mapping
      ↓
Waveform Generation
      ↓
Signal Visualization
```

---

## Supported Modulations

### ASK

Amplitude changes according to symbol value.

Carrier equation:

```math
y(t)=A\sin(2\pi f t + \phi)
```

---

### PSK

Phase changes according to symbol index.

Phase mapping:

```math
\phi_k = \frac{2\pi k}{M}
```

---

### FSK

Carrier frequency changes according to symbol value.

---

### QAM

Uses I/Q mapping and constellation visualization.

QAM equation:

```math
y(t)=I\cos(2\pi ft)-Q\sin(2\pi ft)
```

Supports:
- 4-QAM
- 16-QAM
- 64-QAM

---

## Example Configurations

### 16-QAM

```text
N = 4
M = 16
```

### 64-QAM

```text
N = 6
M = 64
```

---

## Screenshots

### Front Panel

- Real-time waveform display
- QAM constellation visualization
- Dynamic modulation selection

### Block Diagram

- Formula Node based architecture
- Nested loop waveform generation
- Modular signal processing pipeline

---

## Technologies Used

- LabVIEW
- Formula Nodes
- Waveform Graphs
- XY Graphs

---

## Future Improvements

- AWGN noise channel
- BER calculation
- Demodulation
- FFT spectrum analyzer
- Eye diagram
- Gray coding
- Pulse shaping filters
- Constellation animation

---

## Author

Ayoub ETTAIBE 