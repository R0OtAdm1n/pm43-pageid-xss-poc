# Honeywell PM43 Pageid XSS Vulnerability POC

This repository contains a proof-of-concept (POC) code that demonstrates the existence of a Cross-Site Scripting (XSS) vulnerability in PM43 devices through the `pageid` parameter. The vulnerability affects PM43 devices with a version of P10.11.013310 or earlier.

## Prerequisites

To use this XSS vulnerability POC code, ensure that you have the following:

- Go programming language version 1.17 or higher installed on your system.
- Access to a PM43 printer device with the vulnerable version.

## Usage

Follow the steps below to use this XSS vulnerability POC code:

1. Clone or download this repository to your local machine.
2. Open a terminal and navigate to the project directory.

### Single URL Testing

To test a single URL, execute the following command:

```bash
go run main.go -url <target URL>
```

Replace `<target URL>` with the URL of the PM43 printer device you want to test. For example:

```bash
go run main.go -url http://printer.example.com
```

### Multiple URL Testing

If you have a file containing multiple URLs to test, use the following command:

```bash
go run main.go -file <input file>
```

Replace `<input file>` with the path to the file containing the URLs. Each URL should be on a separate line in the file.

## Output

The POC code will send malicious scripts using the `pageid` parameter to the provided URL(s) and analyze the responses. If the XSS vulnerability is present, it will display a success message indicating the detection of the vulnerability and the payload used. If no vulnerability is detected, a failure message will be displayed.

Please note that this POC code specifically targets the `pageid` parameter for XSS testing. Depending on your specific scenario, you may need to consider other input parameters or attack vectors.

## Disclaimer

This XSS vulnerability POC code is provided for educational and testing purposes only. Use it responsibly and ensure that you have proper authorization to test the target device. The author takes no responsibility for any misuse or damage caused by using this POC code.

## License

This XSS vulnerability POC code is licensed under the [MIT License](LICENSE).

## Acknowledgments

This POC code is based on the original code from the OpenAI GPT-3.5 model.

**Use this XSS vulnerability POC code responsibly and with caution. Respect the security and privacy of others.**