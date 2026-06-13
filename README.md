# representus

A simple, mobile-friendly platform for collecting verified community input.

representus is an open source engagement and feedback system designed for organizations that need a trustworthy way to ask questions, gather responses, run polls, and understand what their members, residents, customers, or stakeholders think.

The goal is to make public feedback easier to collect, easier to participate in, and easier to trust.

## Table of Contents

- [Vision](#vision)
- [Core Goals](#core-goals)
- [Example Use Cases](#example-use-cases)
- [Planned Features](#planned-features)
- [What This Project Is Not](#what-this-project-is-not)
- [Guiding Principles](#guiding-principles)
- [Possible Architecture](#possible-architecture)
- [Early Data Model Ideas](#early-data-model-ideas)
- [Roles](#roles)
- [Security Goals](#security-goals)
- [Development Status](#development-status)
- [Roadmap](#roadmap)
- [Installation](#installation)
- [Development](#development)
- [Contributing](#contributing)
- [Good First Issues](#good-first-issues)
- [Example User Stories](#example-user-stories)
- [License](#license)
- [Disclaimer](#disclaimer)

## Vision

Many organizations need feedback from real people, but common tools often have problems:

* Anyone can vote multiple times
* Feedback is scattered across email, social media, meetings, and paper forms
* Participation is hard from a phone
* Results are not always transparent
* People do not know whether their input was actually seen
* Leaders lack a simple way to ask focused questions

This project aims to provide a practical, open source alternative.

It should be easy enough for a PTA, neighborhood group, nonprofit, business, local government, or public agency to use, while still supporting stronger identity verification when needed.

## Core Goals

* Simple to use from a phone
* Accessible to non-technical users
* Open source and self-hostable
* Support verified accounts
* Help reduce duplicate voting
* Allow organizations to ask questions and gather structured feedback
* Make results easier to understand
* Support transparent decision-making
* Keep privacy and security as core design principles

## Example Use Cases

This software could be used by:

* A PTA asking parents to vote on meeting times or budget priorities
* A city council collecting feedback on a proposed ordinance
* A nonprofit polling volunteers about event planning
* A business gathering employee or customer input
* A neighborhood association prioritizing local issues
* A public agency asking residents about service improvements
* A member organization running internal surveys or advisory votes

## Planned Features

### User Registration and Verification

Users should be able to create an account and verify their identity using supported login systems.

Possible authentication options may include:

* Email login
* Magic links
* Passkeys
* SAML
* OAuth / OpenID Connect
* login.gov
* Google Workspace
* Microsoft Entra ID
* Other SSO providers

The system should support the idea of one verified person having one response or vote per question, poll, or issue.

### Organizations

The platform should allow separate organizations to manage their own engagement spaces.

Examples:

* School groups
* Local governments
* Departments
* Committees
* Businesses
* Nonprofits
* Clubs
* Associations

Each organization should be able to create its own questions, polls, groups, and participation rules.

### Questions and Polls

Organizations should be able to create different kinds of public or private input requests.

Possible formats:

* Yes / no questions
* Multiple choice polls
* Ranked choice questions
* Short answer feedback
* Long-form comments
* Issue prioritization
* Sentiment feedback
* Open discussion prompts

### Verified Participation

The project should support controls to help prevent duplicate participation.

Examples:

* One response per verified account
* One vote per verified person
* Optional identity provider enforcement
* Optional organization membership checks
* Optional invite-only participation
* Optional public participation with rate limits

### Mobile-Friendly Interface

The interface should be designed mobile-first.

Users should be able to:

* Register from a phone
* Sign in easily
* Answer questions quickly
* Review open polls
* Submit feedback without confusion
* View results in a readable format

### Accessibility

Accessibility should be a major design requirement, not an afterthought.

The project should aim for:

* Clear language
* Keyboard navigation
* Screen reader support
* Good color contrast
* Large tap targets
* Responsive layouts
* Minimal clutter
* Plain-language instructions

### Results and Transparency

Organizations should be able to publish results in a clear and understandable way.

Possible result views:

* Vote totals
* Percentages
* Charts
* Response summaries
* Public reports
* Exportable data
* Anonymous comment summaries

The platform should make it clear when results are public, private, anonymous, or restricted.

### Privacy

The platform should be designed to collect only the information needed for each use case.

Important privacy goals:

* Avoid unnecessary personal data collection
* Separate identity verification from public responses where possible
* Support anonymous or pseudonymous feedback when appropriate
* Make participation rules clear before a user responds
* Allow organizations to configure data retention policies
* Protect user data from unnecessary exposure

## What This Project Is Not

This project is not intended to replace official election systems.

It is intended for engagement, advisory voting, surveys, feedback, polling, prioritization, and community input.

Organizations should not use this software for binding public elections unless it has been independently reviewed, secured, audited, and approved for that purpose by the appropriate authorities.

## Guiding Principles

### Simple First

The platform should be easy for regular people to use without training.

### Trustworthy by Design

Users should understand who is asking the question, who can participate, how responses are counted, and how results are shared.

### Open Source

The software should be inspectable, reusable, and improvable by the community.

### Flexible Identity

Different organizations have different verification needs. A PTA may only need email verification. A government agency may require login.gov or another trusted identity provider.

### Mobile Access

Participation should not require a desktop computer.

### Privacy Respecting

Verification should not mean unnecessary public exposure of personal identity.

## Possible Architecture

The final stack has not been decided yet.

Potential components may include:

* Web frontend
* Backend API
* Database
* Authentication provider integration
* Admin dashboard
* Organization management
* Polling and feedback engine
* Reporting and export tools

Possible technologies:

* Python / Django
* Django REST Framework
* PostgreSQL
* Vue / Quasar
* Tailwind CSS
* Docker
* OpenID Connect / OAuth2
* SAML support

## Early Data Model Ideas

Possible core objects:

* User
* Organization
* Organization Member
* Identity Provider
* Question
* Poll
* Response
* Vote
* Comment
* Result
* Audit Log
* Invitation
* Role / Permission

## Roles

Possible roles may include:

* Platform administrator
* Organization administrator
* Moderator
* Question creator
* Verified participant
* Public viewer

## Security Goals

Security should be considered from the start.

Important areas:

* Secure authentication
* Strong session management
* CSRF protection
* Rate limiting
* Abuse prevention
* Permission checks
* Audit logging
* Safe exports
* Protection against duplicate voting
* Protection against ballot stuffing
* Protection against unauthorized result changes

## Development Status

This project is in the planning and early development stage.

The README currently describes the intended direction of the software. Features, architecture, and implementation details are expected to change as the project develops.

## Roadmap

### Phase 1: Planning

* Define core use cases
* Choose initial tech stack
* Create basic wireframes
* Define data model
* Define authentication strategy
* Define contribution guidelines

### Phase 2: Prototype

* Create basic app structure
* Add organization support
* Add user registration
* Add basic authentication
* Create simple question/poll flow
* Allow users to submit one response
* Display basic results

### Phase 3: Verification

* Add SSO support
* Add OpenID Connect support
* Explore login.gov compatibility
* Add organization membership controls
* Add duplicate participation protections

### Phase 4: Admin and Reporting

* Add admin dashboard
* Add question management
* Add result publishing controls
* Add CSV export
* Add basic charts
* Add audit logs

### Phase 5: Accessibility and Hardening

* Improve mobile UI
* Improve screen reader support
* Add automated tests
* Add security review checklist
* Add deployment documentation
* Add privacy documentation

## Installation

Installation instructions will be added once the initial application structure is available.

Planned deployment options may include:

* Local development setup
* Docker Compose
* Self-hosted Linux server
* Cloud deployment examples

## Development

Development instructions will be added as the project is built.

Expected future commands may include:

```bash
git clone https://github.com/silversword411/representus.git
cd representus
```

Then follow the setup instructions for the selected stack.

## Contributing

Contributions are welcome once the project structure is in place.

Useful areas for contribution may include:

* Backend development
* Frontend development
* Accessibility review
* Authentication and SSO integration
* Security review
* Documentation
* UX design
* Mobile interface testing
* Civic technology research
* Deployment examples

Before contributing, please open an issue to discuss major changes.

## Good First Issues

Potential starter tasks:

* Improve this README
* Create logo ideas
* Draft user stories
* Draft database models
* Research login.gov integration requirements
* Create wireframes
* Define accessibility checklist
* Define privacy checklist
* Create sample poll flows

## Example User Stories

As an organization administrator, I want to create a question so that I can collect feedback from verified participants.

As a participant, I want to answer from my phone so that I can give input quickly.

As a participant, I want to know whether my response is anonymous so that I understand what information is being shared.

As an organization administrator, I want to limit each person to one response so that results are more trustworthy.

As a public viewer, I want to see published results so that I can understand what the community said.

As a moderator, I want to review comments so that abusive or off-topic content can be handled appropriately.

## License

This project is released as open source under the [MIT License](LICENSE).

## Disclaimer

This software is intended for civic engagement, organizational feedback, surveys, advisory voting, and public input.

It is not designed or certified for official government elections or legally binding voting systems.
