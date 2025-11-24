**Loafr v0.1 -- Test Execution Report**

**Project:** Loafr v0.1**\
Test Executor:** Ashmitha A**s**hokkumar, Sivapriya Gopi, Shivani
Mahadik**\
Execution Date:** 19-Nov-2025**\
Environment:** Python 3.11.4, pytest 9.0.1, Windows 10**\
Log / Output Reference:** pytest -v console output

**Group 1: Log Loading Tests**

+-------------------+-------------------------------+-------------------+-------------------+--------------------------------------------------------+
| **Test ID**       | **Test Name**                 | **Acceptance      | **Result**        | **Console Output**                                     |
|                   |                               | Criteria**        |                   |                                                        |
+===================+===============================+===================+===================+========================================================+
| TC1               | test_load_valid_logfile       | A.C1.1, A.C1.5    | PASS              | tests/test_filtering.py::test_load_valid_logfile       |
|                   |                               |                   |                   |                                                        |
|                   |                               |                   |                   | PASSED \[ 4%\]                                         |
+-------------------+-------------------------------+-------------------+-------------------+--------------------------------------------------------+
| TC2               | test_invalid_json_skipped     | A.C1.2            | PASS              | tests/test_filtering.py::test_invalid_json_skipped     |
|                   |                               |                   |                   | PASSED \[ 8%\]                                         |
+-------------------+-------------------------------+-------------------+-------------------+--------------------------------------------------------+
| TC3               | test_missing_mandatory_fields | A.C1.3            | PASS              | tests/test_filtering.py::test_missing_mandatory_fields |
|                   |                               |                   |                   | PASSED \[ 12%\]                                        |
+-------------------+-------------------------------+-------------------+-------------------+--------------------------------------------------------+
| TC16              | test_empty_logfile            | A.C1.1            | PASS              | tests/test_filtering.py::test_empty_logfile            |
|                   |                               |                   |                   |                                                        |
|                   |                               |                   |                   | PASSED \[ 64%\]                                        |
+-------------------+-------------------------------+-------------------+-------------------+--------------------------------------------------------+
|                                                                                                                                                    |
+----------------------------------------------------------------------------------------------------------------------------------------------------+

**Group 2: Filtering Tests**

  -------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Test   **Test Name**                                      **Acceptance   **Result**   **Console Output**
  ID**                                                        Criteria**                  
  -------- -------------------------------------------------- -------------- ------------ ---------------------------------------------------------------------------
  TC4      test_filter_by_component_and_type_component_only   A.C2.1         PASS         tests/test_filtering.py::test_filter_by_component_and_type_component_only
                                                                                          PASSED \[ 16%\]

  TC5      test_filter_by_component_and_type_none_found       A.C2.1         PASS         tests/test_filtering.py::test_filter_by_component_and_type_none_found
                                                                                          PASSED \[ 20%\]

  TC6      test_filter_by_component_and_type_type_only        A.C2.1         PASS         tests/test_filtering.py::test_filter_by_component_and_type_type_only PASSED
                                                                                          \[ 24%\]

  TC7      test_filter_by_component_and_type_empty_result     A.C2.1         PASS         tests/test_filtering.py::test_filter_by_component_and_type_empty_result
                                                                                          PASSED \[ 28%\]

  TC8      test_numeric_filter_single_hit                     A.C2.2         PASS         tests/test_filtering.py::test_numeric_filter_single_hit PASSED \[ 32%\]

  TC9      test_numeric_filter_ignores_non_numbers            A.C2.3         PASS         tests/test_filtering.py::test_numeric_filter_ignores_non_numbers PASSED \[
                                                                                          36%\]

  TC17     test_numeric_all_below_threshold                   A.C2.2         PASS         tests/test_filtering.py::test_numeric_all_below_threshold PASSED \[ 68%\]

  TC18     test_numeric_missing_field                         A.C2.3         PASS         tests/test_filtering.py::test_numeric_missing_field PASSED \[ 72%\]

  TC22     test_filter_component_type_no_match                A.C2.1         PASS         tests/test_filtering.py::test_filter_component_type_no_match PASSED \[
                                                                                          88%\]

  TC23     test_log_entry_extra_fields                        A.C2.4         PASS         tests/test_filtering.py::test_log_entry_extra_fields PASSED \[ 92%\]

  TC25     test_numeric_exact_threshold                       A.C2.2         PASS         tests/test_filtering.py::test_numeric_exact_threshold PASSED \[100%\]
  -------------------------------------------------------------------------------------------------------------------------------------------------------------------

**Group 3: Timestamp Parsing Tests**

+-------------------+-----------------------------------+-------------------+-------------------+------------------------------------------------------------+
| **Test ID**       | **Test Name**                     | **Acceptance      | **Result**        | **Console Output**                                         |
|                   |                                   | Criteria**        |                   |                                                            |
+===================+===================================+===================+===================+============================================================+
| TC10              | test_timestamp_parsing_valid      | A.C1.5            | PASS              | tests/test_filtering.py::test_timestamp_parsing_valid      |
|                   |                                   |                   |                   | PASSED \[ 40%\]                                            |
+-------------------+-----------------------------------+-------------------+-------------------+------------------------------------------------------------+
| TC11              | test_timestamp_parsing_invalid    | A.C1.5            | PASS              | tests/test_filtering.py::test_timestamp_parsing_invalid    |
|                   |                                   |                   |                   | PASSED \[ 44%\]                                            |
+-------------------+-----------------------------------+-------------------+-------------------+------------------------------------------------------------+
| TC24              | test_parse_timestamp_milliseconds | A.C1.5            | PASS              | tests/test_filtering.py::test_parse_timestamp_milliseconds |
|                   |                                   |                   |                   | PASSED \[ 96%\]                                            |
+-------------------+-----------------------------------+-------------------+-------------------+------------------------------------------------------------+
|                                                                                                                                                            |
+------------------------------------------------------------------------------------------------------------------------------------------------------------+

**Group 4: Time-Window Response Analysis Tests**

+--------+----------------------------------------+--------------+------------+-----------------------------------------------------------------+
| **Test | **Test Name**                          | **Acceptance | **Result** | **Console Output**                                              |
| ID**   |                                        | Criteria**   |            |                                                                 |
+========+========================================+==============+============+=================================================================+
| TC12   | test_response_arrives_in_time          | A.C3.1,      | PASS       | tests/test_filtering.py::test_response_arrives_in_time PASSED   |
|        |                                        | A.C3.2,      |            | \[ 48%\]                                                        |
|        |                                        | A.C3.3       |            |                                                                 |
+--------+----------------------------------------+--------------+------------+-----------------------------------------------------------------+
| TC13   | test_response_missing                  | A.C3.1,      | PASS       | tests/test_filtering.py::test_response_missing PASSED \[ 52%\]  |
|        |                                        | A.C3.2,      |            |                                                                 |
|        |                                        | A.C3.3       |            |                                                                 |
+--------+----------------------------------------+--------------+------------+-----------------------------------------------------------------+
| TC14   | test_response_too_late                 | A.C3.1,      | PASS       | tests/test_filtering.py::test_response_too_late PASSED          |
|        |                                        | A.C3.2,      |            |                                                                 |
|        |                                        | A.C3.3       |            | \[ 56%\]                                                        |
+--------+----------------------------------------+--------------+------------+-----------------------------------------------------------------+
| TC15   | test_multiple_triggers_partial_missing | A.C3.1,      | PASS       | tests/test_filtering.py::test_multiple_triggers_partial_missing |
|        |                                        | A.C3.3,      |            | PASSED \[ 60%\]                                                 |
|        |                                        | A.C3.4       |            |                                                                 |
+--------+----------------------------------------+--------------+------------+-----------------------------------------------------------------+
| TC19   | test_multiple_responses_one_trigger    | A.C3.4       | PASS       | tests/test_filtering.py::test_multiple_responses_one_trigger    |
|        |                                        |              |            | PASSED \[ 76%\]                                                 |
+--------+----------------------------------------+--------------+------------+-----------------------------------------------------------------+
| TC20   | test_multiple_triggers_no_responses    | A.C3.1,      | PASS       | tests/test_filtering.py::test_multiple_triggers_no_responses    |
|        |                                        | A.C3.3       |            | PASSED \[ 80%\]                                                 |
+--------+----------------------------------------+--------------+------------+-----------------------------------------------------------------+
| TC21   | test_response_at_window_edge           | A.C3.2,      | PASS       | tests/test_filtering.py::test_response_at_window_edge PASSED \[ |
|        |                                        | A.C3.3       |            | 84%\]                                                           |
+--------+----------------------------------------+--------------+------------+-----------------------------------------------------------------+

**Summary**

Total Tests: 25

Passed: 25

Failed: 0

Coverage: Full coverage of User Stories US1, US2, US3

Output / Log Reference: Console output from pytest -v or optional
test_output.log

![](media/image1.png){width="6.283333333333333in"
height="2.020138888888889in"}

![](media/image2.png){width="6.283333333333333in" height="2.25625in"}
