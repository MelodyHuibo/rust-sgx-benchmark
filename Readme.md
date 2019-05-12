# Instructions

```
cd mesalock-sgx-bench
./test_perf.sh
cd ..

cd rust-linux
./test_perf.sh
cd ..

cd fortanix-sgx-bench
./test_perf.sh
cd ..

cd c-sgx-bench
./test_perf.sh
cd ..

cd c-linux-bench
./test_perf.sh
cd ..
```

Then process the generated results.txt


# Results

## Yu's 9900k+64GB Non ECC desktop. 2.5 toolchain

|                          | ML-Rust-SGX| Fortanix-Rust-SGX | Rust-Linux  | C-SGX    | C-Linux |
| ------------------------ | ---------- | ----------------- | ----------- | -------- | ------- |
|  fann                    | 21.16858   |    24.50          |  23.20      | 19.66372 | 19.59   |
|  fasta                   | 25.25682   |    28.25          |  26.99      | 28.42409 | 0.52    |
|  mandel                  | 4.64135    |    6.67           |  5.10       | 4.23488  | 0.20    |
|  nbody                   | 28.43456   |    30.67          |  29.89      | 28.42409 | 31.68   |
| spectum                  | 23.23975   |    25.57          |  26.83      | 17.2588  | 17.47   |
| localattest              | 19.49004   |                   |             | 19.47614 |         |
| switchless-normal-ocall  | 9.98110    |                   |             | 9.889182 |         |
| switchless-ocall         | 1.02866    |                   |             | 1.099590 |         |
| switchless-normal-ecall  | 11.82719   |                   |             | 11.594337|         |
| switchless-ecall         | 1.39487    |                   |             | 1.587854 |         |
