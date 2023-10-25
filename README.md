
# LBO Model in Python

This is a complete rework of Calivala-86's repo, as I have found serveral functions (or classes so the code would be easier to maintain + better modularity) that could be improved, and cleaned up some variable names("entry_ass" is funny enough for me to get distracted). Also utilising some new libraries like Polars to improve the performance.

Note that this is written in Python on Jupyter Notebook.

Most importantly, I'm turning it into a monthly statement instead of annually,
as I have never once asked to do an annual statement at work ever.
The IRR is different from the what the casestudy has provided,
as I saw that they didn't incorpate the acquisition cost and the exit value into the cashflow.
Weird.

**Original description**:
> This is a simple replication/recreation of the PAPER LBO MODEL EXAMPLE by STREETOFWALLS using Python. The rationale behind for using Python was to understand how effieciently Python can be compare to excel in sense of timing assumption and formula manipulation.

## Installation & Dependencies

If you're using VSCode, install **Jupyter Notebook's extensions**.

1. Clone this repo:
`git clone https://github.com/larrysammii/LBO-model-Python`
2. Start a venv:
`python3 -m venv env`
3. Activate venv:
`source env/bin/activate`
4. Install dependencies:
`pip install -r requirements.txt`.

### Libraries needed

- Numpy_financial
- Polars

## Dataset & Case Study

- [StreetOfWalls' LBO modelling test example](https://www.streetofwalls.com/finance-training-courses/private-equity-training/lbo-modeling-test-example/)

## About using Polars instead of Pandas

Pandas has been around for quite a while now and if you have used it you know it could be slow when you have large amount of data.

I'm using Polars instead of Pandas in this project just because it's FAST. There are some differences in syntaxes but I think it's the best to use whichever has better performance.

(Update: Pandas 2.0 is out, with pyarrow backend, it's much faster now, very comparable with Polars.)
(Update 2: I'm in too deep with Polars on this project to switch back to Pandas.)

Also, Polars is a column-based-no-index library (which the creators of Polars [argued that indices are unnecessary](https://github.com/pola-rs/polars/issues/2243), and I agreed.).

## Acknowledgement

- [Calivala-86's original repo](https://github.com/Calivala-86/PE-LBO-MODEL.git)
