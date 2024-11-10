# Math Syntax Linter

A Python utility to automatically convert LaTeX-style math delimiters to MathJax-style delimiters in Markdown files. This tool is particularly useful for maintaining consistency in mathematical notation across documentation and educational content.

## Features

- Recursively processes all `.md` files in a specified directory
- Converts inline math expressions from `\( expr \)` to `$expr$`
- Converts display math expressions from `\[ expr \]` to `$$(expr)$$`
- Preserves original file content while only updating math syntax
- Provides progress information during processing
- Handles spaces in mathematical expressions correctly

## Usage

1. Clone the repository:
```bash
git clone https://github.com/yourusername/math-syntax-linter.git
cd math-syntax-linter
```

2. Update the directory path in `math_linter.py`:
```python
directory = Path("/path/to/your/markdown/files")
```

3. Run the script:
```bash
python math_linter.py
```

## Example Conversions

### Inline Math
Before:
```
This is an inline expression \( x^2 + y^2 = z^2 \)
```

After:
```
This is an inline expression $x^2 + y^2 = z^2$
```

### Display Math
Before:
```
This is a display expression:
\[ E = mc^2 \]
```

After:
```
This is a display expression:
$$(E = mc^2)$$
```

## Requirements

- Python 3.6 or higher
- No external dependencies required

## Project Structure

```
math-syntax-linter/
├── math_linter.py
├── README.md
└── LICENSE
```

## How It Works

The script uses regular expressions to identify and convert mathematical expressions:

1. Searches for patterns matching `\( expr \)` and `\[ expr \]`
2. Ensures proper spacing is maintained
3. Converts to the appropriate MathJax syntax
4. Updates files only if changes are needed

## Error Handling

The script includes robust error handling:
- Verifies directory existence
- Reports processing errors for individual files
- Maintains original content in case of processing failures

## Contributing

Contributions are welcome! Here are some ways you can contribute:

1. Report bugs
2. Suggest new features
3. Submit pull requests

Please ensure that your pull requests:
- Include clear descriptions
- Add appropriate tests
- Follow existing code style

## Future Improvements

- [ ] Add backup creation before modifications
- [ ] Implement file exclusion patterns
- [ ] Add dry run mode
- [ ] Support for custom delimiter patterns
- [ ] Add detailed logging options

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Author

[Your Name]

## Acknowledgments

- Inspired by the need to maintain consistent mathematical notation in documentation
- Thanks to the Python community for regex support
