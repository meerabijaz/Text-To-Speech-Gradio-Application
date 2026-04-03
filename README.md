# Text-to-Speech Notebook

This Jupyter notebook implements a Text-to-Speech (TTS) application using the SpeechT5 model from Microsoft, integrated with a Gradio web interface.

## Features

- Convert text to speech using advanced TTS models
- Multiple speaker voices available (Female and Male options)
- Web-based interface for easy interaction
- Audio output in WAV format

## Requirements

- Python 3.7+
- Jupyter Notebook
- Internet connection for downloading models and data

## Dependencies

The notebook installs the following packages automatically:

- transformers
- gradio
- soundfile
- sentencepiece
- huggingface_hub
- torch (PyTorch)

## Setup and Installation

1. Ensure you have Python and Jupyter Notebook installed.
2. Open the `gradio-tts.ipynb` file in Jupyter Notebook or JupyterLab.
3. Run the first cell to install the required dependencies:
   ```
   !pip install -q transformers gradio soundfile sentencepiece huggingface_hub
   ```

## Usage

1. Execute the cells in order from top to bottom.
2. The notebook will download the necessary models and speaker embeddings (this may take some time on first run).
3. Once all cells are executed, the Gradio interface will launch.
4. In the web interface:
   - Enter your text in the input box
   - Select a speaker voice from the dropdown
   - Click "Synthesize" to generate speech
   - Listen to the generated audio

## Notes

- The notebook uses speaker embeddings from the CMU Arctic dataset.
- Audio is generated at 16kHz sample rate.
- Long texts are automatically truncated to fit the model's token limit.
- The interface will be accessible via a local URL and optionally shareable.

## Troubleshooting

- If you encounter CUDA-related errors, the notebook will fall back to CPU.
- Ensure you have sufficient disk space for model downloads (~1-2GB).
- If the Gradio interface doesn't launch, check your firewall settings.
