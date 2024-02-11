## Beyond Pandas: A dive into Python's high-performance dataframe library *Polars* - Presentation for PythonPune meetup dated 10 Feb 2024

![banner](/assets/polars_banner.jpg)

### Some basics about Polars

- Based on the principle of RDBS engines' query optimisation. 

- Written in Rust to provide _performance, parallelism and efficient memory management_ out of the box.

- Can perform operations over larger than RAM size of data through `Lazy` mode.

- `Strict typing` (datatyping) lets the errors to be caught before performing operations on the data, just like `Rust` and other low level languages. 

- Not just a mere dataframe library, more of a
> **... Query Engine with a dataframe frontend** - _Ritchie Vink, EuroPy 2023_


### What I like about Polars? 
- *Readability* - `.lower()` can mean n things, but `to_lower()` means only what it supposed to mean.
- No more index anymore :tada:. Seriously, after Pandas, the forceful inclusion of index based operations has became a normal, and I hated every minute of it.
- *Expr* everywhere. You are not writing Python code anymore for most of the operations, but the python binding of the **Rust Expression**.
- *Optimisation* - one less thing to think about when I write the code. 
- Community support - Even though the library is comparatively new, the community is very active in [discord](https://discord.gg/rjAmwfY6). You can get answer within a day, for anything, *literally anything*. 

### Where did I struggle with Polars?
- *Steep learning curve* - As it is one of a kind of tool/utility/library, you definitely have to learn the `Polar way`, which may not be simple for everyone. 


### Demonstration

Data - https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

- Data preparation 
  - Modification of data types
  - Usage of `with_columns`
  - data selection with `select` and `col`
  - Copy with `col` and `alias`

- Data analysis
  - `groupby` and `agg`


### Resources
- [Polars documentation](https://docs.pola.rs/py-polars/html/reference/index.html)
- [A bird's eye view of Polars](https://pola.rs/posts/polars_birds_eye_view/)
- [Getting started with Polars](https://youtu.be/CJ0f45evuME?si=VlWM7PzHVMziMx2i)
- [Keynote - Euro SciPy - 2023](https://youtu.be/GTVm3QyJ-3I?si=0UBj7SIIYLlrliCM)
