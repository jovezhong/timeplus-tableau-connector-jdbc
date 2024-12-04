# Timeplus Tableau JDBC connector

## Intro

This is an extension for Tableau Desktop / Tableau Server that simplifies the process of connecting Tableau to Timeplus and extends support for standard Tableau functionality when working with Timeplus (as compared to Generic ODBC/JDBC)

## Features

- In comparison with **Other Databases (ODBC)**: this connector uses the JDBC driver, which is faster than the ODBC driver in some cases (for example, creating Extracts), and is also much easier to install than ODBC (a cross-platform jar file, which does not require compiling for individual platforms).
- In comparison with **Other Databases (JDBC)**: this connector has fine-tuning SQL queries to implement most of the standard Tableau functionality (including multiple JOINS in the data source, Sets, etc.), and it has a friendly connection dialog ;)

## Before you install

Requirements
- Tableau **2020.4+**
- Timeplus Enterprise **2.4+**

## Installation (Tableau Desktop)
1. Download the [Timeplus JDBC Driver](https://github.com/timeplus-io/timeplus-native-jdbc) (version 2.0.7 required), and place the `timeplus-native-jdbc-shaded-2.0.7.jar` to:
    - macOS: `~/Library/Tableau/Drivers`
    - Windows: `C:\Program Files\Tableau\Drivers`
    - You need to create the folder if it doesn't already exist
2. Download the latest `timeplus-jdbc.taco` from the [Releases](https://github.com/timeplus-io/timeplus-tableau-connector-jdbc/releases) page, and place it to:
    - macOS: `~/Documents/My\ Tableau\ Repository/Connectors`
    - Windows: `C:\Users\[Windows User]\Documents\My Tableau Repository\Connectors`
3. Run Tableau Desktop
4. In Tableau Desktop: **Connect** ➔ **To a Server** ➔ **Timeplus JDBC by Timeplus, Inc.**

## Future plans
- Publishing the connector at [exchange.tableau.com](https://exchange.tableau.com/connectors)

## Tests
The connector is being tested with the [TDVT framework](https://tableau.github.io/connector-plugin-sdk/docs/tdvt) and currently maintains a 97% coverage ratio.

## Acknowledgement

This repo is forked from https://github.com/ClickHouse/clickhouse-tableau-connector-jdbc.
