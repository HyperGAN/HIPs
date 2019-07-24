---
hip: 1
title: HIP Purpose and Guidelines
status: Active
created: 2019-07-24
---

## What is an HIP?

HIP stands for HyperGAN Improvement Proposal. A HIP is a design document providing information to the HyperGAN community, or describing a new feature for HyperGAN or its processes or usages. The HIP should provide a concise technical specification of the feature and a rationale for the feature. The HIP author is responsible for building consensus within the community and documenting dissenting opinions.

## HIP Rationale

We intend HIPs to be the primary mechanisms for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have gone into HyperGAN.  Because the HIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

It is highly recommended that a single HIP contain a single key proposal or new idea. The more focused the HIP, the more successful it tends to be. A change to a configuration or new configuration option doesn't require a HIP; a new `hypergan command` or compiled model format, does.

A HIP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate unduly, unless the enhancement is behind a configuration option.

## HIP Work Flow

### Shepherding a HIP

Parties involved in the process are you, the champion or *HIP author*, the [*HIP editors*](#hip-editors), and the [*HyperGAN Core Developers*](https://github.com/HyperGAN/HyperGAN).

It will be your role as the author to make your idea clear to reviewers and interested parties, as well as inviting editors, developers and community to give feedback on the pull request.

### HIP Process 

Following is the process that a successful HIP will move along:

```
[ WIP ] -> [ DRAFT ] -> [ ACCEPTED ] -> [ IMPLEMENTED ] -> [ RELEASED ]
```

Each status change is requested by the HIP author and reviewed by the HIP editors. Use a pull request to update the status. 

* **Draft** - a HIP that is undergoing rapid iteration and changes.
* **Accepted** - The changes have been accepted as part of the HyperGAN roadmap.
* **Implemented** - The changes have been intergrated in HyperGAN and are ready for release.
* **Released** - The changes are released in the latest HyperGAN library.
* **Active** -- Some Informational and Process HIPs may also have a status of “Active” if they are never meant to be completed. E.g. HIP 1 (this HIP).

Other exceptional statuses include:

* **Abandoned** -- This HIP is no longer pursued by the original authors or it may not be a (technically) preferred option anymore.
* **Rejected** -- A HIP that is fundamentally broken, cannot be implemented or does not fit with HyperGAN's abstractions easily enough.
* **Superseded** -- An HIP which was previously final but is no longer considered state-of-the-art. Another HIP will be in Final status and reference the Superseded HIP.

## What belongs in a successful HIP?

Please see the `hip-template.md`

## HIP Formats and Templates

HIPs should be written in [markdown] format.
Image files should be included in a subdirectory of the `assets` folder for that HIP as follows: `assets/hip-N` (where **N** is to be replaced with the HIP number). When linking to an image in the HIP, use relative links such as `../assets/hip-1/image.png`.

## HIP Header Preamble

Each HIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.

` eip:` <HIP number> (this is determined by the HIP editor)

` title:` <HIP title>

` status:` <Draft | Accepted | Implemented | Released | Active | Abandoned | Rejected | Superseded>

` * type:` <Code | Standards | Meta>

` * citations:` URLs to any papers or research

` created:` <date created on>

` * updated:` <comma separated list of dates>

` * requires:` <HIP number(s)>

` * replaces:` <HIP number(s)>

` * superseded-by:` <HIP number(s)>

` * resolution:` \<a url pointing to the resolution of this HIP\>

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header optionally lists the names, email addresses or usernames of the authors/owners of the HIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:

This field is optional.

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

if the email address or GitHub username is included, and

> Random J. User

if the email address is not given.

#### `type` header

The `type` header specifies the type of HIP: Code | Standards | Meta 

#### `category` header

The `category` header specifies the HIP's category. This is required for standards-track HIPs only.

#### `created` header

The `created` header records the date that the HIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

#### `updated` header

The `updated` header records the date(s) when the HIP was updated with "substantial" changes. This header is only valid for HIPs of Draft and Active status.

#### `requires` header

HIPs may have a `requires` header, indicating the HIP numbers that this HIP depends on.

## Auxiliary Files

HIPs may include auxiliary files such as diagrams. Such files must be named HIP-XXXX-Y.ext, where “XXXX” is the HIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

## Transferring HIP Ownership

It occasionally becomes necessary to transfer ownership of HIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred HIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the HIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the HIP. We try to build consensus around an HIP, but if that's not possible, you can always submit a competing HIP.

If you are interested in assuming ownership of an HIP, send a message asking to take over, addressed to both the original author and the HIP editor. If the original author doesn't respond to email in a timely manner, the HIP editor will make a unilateral decision (it's not like such decisions can't be reversed :)).

## HIP Editor Responsibilities

For each new HIP that comes in, an editor does the following:

- Read the HIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the HIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style

If the HIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the HIP is ready for the repository, the HIP editor will:

- Assign an HIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this HIP)

- Merge the corresponding pull request

- Send a message back to the HIP author with the next step.

Many HIPs are written and maintained by developers with write access to the Ethereum codebase. The HIP editors monitor HIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on HIPs. We merely do the administrative & editorial part.

## History

This document was derived heavily from [Ethereum's EIP-1], which was derived from [Bitcoin's BIP-0001] written by Amir Taaki which in turn was derived from [Python's PEP-0001]. In many places text was simply copied and modified. Although the PEP-0001 text was written by Barry Warsaw, Jeremy Hylton, and David Goodger, they are not responsible for its use in the Ethereum Improvement Process, and should not be bothered with technical questions specific to Ethereum or the HIP. Please direct all comments to the HIP editors.

July 24, 2019: Forked and customized from EIP

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

