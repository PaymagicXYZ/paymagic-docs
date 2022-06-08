# 👐 Introduction

## Introduction

The Paymagic Automate API allows DAOs & crypto teams to automate frequent payouts to their community like running payroll, paying out bounties, funding grants, issuing rewards, or reimbursing expenses.

The Automate API is a simple RESTful API that can be used with any web app/Airtable/Notion/Discord/etc so that crypto teams don’t have to spend countless hours formatting transactions or getting multiple signatures and can focus on their core product instead.

The service revolves around a **Smart Payout Account** which is a customized [Gnosis Safe](https://gnosis-safe.io/) with a 1 of 2 multi-sig threshold where the customer controls one key and Paymagic controls the other. A Smart Payout Account allows automated transaction execution, batching, fraud prevention, gas management, and cross-chain execution.

![Smart Payout Account: Onchain Architecture](<.gitbook/assets/Paymagic Automate@2x(2).png>)
