HEy


[![from_flaxo with_♥](https://img.shields.io/badge/from_flaxo-with_♥-blue.svg)](https://github.com/tcibinan/flaxo)

## Configuration

Source structure should be the following. All `.cpp` scripts should be located under `src/main/cpp` directory.
All tests for a single cpp file should be located under corresponding directory `src/test/resources/script_name`.
Each test is basically a directory with two txt files `input.txt`  and `output.txt`.

```
src/
    main/
        cpp/
            main.cpp
            script1.h
            script1.cpp
            script2.h
            script2.cpp
    test/
        resources/
            script1/
                some_test_case/
                    input.txt
                    output.txt
            script2/
                test_case/
                    input.txt
                    output.txt
                another_test_case/
                    input.txt
                    output.txt
    run_tests.sh
```

Success output
```
Tests

> script1
PASSED: some_test_case

> script2
PASSED: test_case
PASSED: another_test_case

Summary: SUCCESS
```

Failure output
```
Tests

> script1
PASSED: some_test_case

> script2
FAILED: test_case: On input [-3 -6] was [-9] but expected [-7].
PASSED: another_test_case

Summary: FAIL
```

## Demo

To run tests for scripts `plus` and `minus`
```bash
./run_tests.sh plus minus
```

Expected output
```
Tests:

> plus:
PASSED: negative_numbers
PASSED: positive_numbers

> minus:
PASSED: negative_result

Summary: SUCCESS
```
