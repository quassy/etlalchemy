1. Add regression tests
2. Add unit tests
3. Drop support for Python <3.7
4. Check to see if FK exists between 2 tables - if it does, append an integer to the end of the
   constraint_name. Right now we just catch exceptions, and only on a subset of supported RDBMSs (
   OperationalError - MySQL, ProgrammingError - PostgreSQL)
5. Replace column-type guessing process (iterating over every row)  with a GROUP BY query to improve
   performance.
6. Add parameter for "_quoted_strings_enclosed_by_" to **ETLAlchemySource** to override default .csv
   quote-character.
7. Add parameter for "_cleanup_table_csv_files_", with default value of True, allowing the user to
   override default and let files persist after they are loaded into Target DB.
8. Check if two phase migrate should be
   included https://github.com/seanharr11/etlalchemy/pull/34/files
9. Check if binary type should be
   supported https://github.com/tpow/etlalchemy/commit/3afb41ca4304d94f3a544532efa5ed663d3458f2
10. Check various fixes and enhancements https://github.com/seanharr11/etlalchemy/pull/39
11. Support Python 3.10
12. Support sqlalchemy 2.0
13. Switch to Poetry
14. Black everything
15. Fix all flake8 errors
16. Publish as package on PyPI
