# JobPortal Smart Contract

This smart contract implements a decentralized job portal on the Ethereum blockchain. It allows administrators to manage job listings and applicants, while enabling job seekers to apply for positions and receive ratings.

## Features

- Add new job applicants (admin only)
- Retrieve applicant details
- Get applicant type based on domain
- Add new job listings (admin only)
- Retrieve job details based on job role
- Allow applicants to apply for jobs
- Provide and retrieve applicant ratings

## Contract Details

- **SPDX-License-Identifier:** MIT
- **Solidity Version:** 0.8.24

## Structures

### Applicant
- `id`: Unique identifier for the applicant
- `name`: Name of the applicant
- `age`: Age of the applicant
- `expectedJobType`: Type of job the applicant is looking for
- `skills`: Array of skills possessed by the applicant
- `domain`: Domain or field of expertise

### JobDescription
- `companyName`: Name of the company offering the job
- `jobRole`: Title or role of the job
- `requiredExperience`: Experience required for the position
- `salaryPerAnnum`: Annual salary offered
- `workLocationType`: Type of work location (e.g., remote, on-site)
- `openings`: Number of available positions

## Key Functions

1. `addJobApplicant`: Allows admin to add a new job applicant
2. `getApplicantDetails`: Retrieves details of a specific applicant
3. `getApplicantType`: Returns the domain/type of an applicant
4. `addJob`: Allows admin to add a new job listing
5. `getJobDetails`: Retrieves job details based on job role
6. `applyForJobs`: Enables applicants to apply for available jobs
7. `getAppliedJobs`: Retrieves the jobs an applicant has applied for
8. `giveApplicantRating`: Assigns a rating to an applicant
9. `getApplicantRating`: Retrieves the rating of an applicant

## Usage

1. Deploy the contract to the Ethereum network.
2. The deploying address becomes the admin.
3. Admin can add job applicants and job listings.
4. Applicants can apply for jobs using their unique ID.
5. Admin or authorized parties can provide ratings to applicants.

## Security

- Only the admin (contract owner) can add new applicants and job listings.
- The contract uses function modifiers to restrict admin-only functions.

## Limitations

- The contract does not implement a mechanism for updating or removing job listings or applicants.
- There's no built-in verification of applicant information or job details.
- The rating system is basic and does not include mechanisms to prevent spam or ensure fairness.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
