# Keys to successful privacy threat modeling



Privacy is important! This has been underlined by the GDPR and other data protection legislation that entered into force in the past years and that highlight the need for privacy integration in the software development lifecycle. 

The privacy-by-design principle requires privacy to be included early on in the development lifecycle. But how can this be done in practice? Threat modeling, a systematic approach to reason about what can go wrong in a system, has proven its value in security engineering, and is equally useful for privacy. To get the most out of your privacy threat modeling experience, there are however some simple, yet important, rules you should take into account. 

 The key aspects listed below follow from our experiences with [LINDDUN](https://www.linddun.org), however they are applicable to privacy threat modeling in general, independent of the specific approach or knowledge base that you want to apply.

> *[LINDDUN](https://www.linddun.org) provides a structured process for threat modeling enriched with an extensive privacy knowledge base. It was inspired by Microsoft’s STRIDE and therefore roughly shares the same steps yet focusing on the 7 privacy threat categories that are contained in its acronym (i.e. linkability, identifiability, non-repudiation, detectability, disclosure of information, unawareness, non-compliance). [LINDDUN GO](https://www.linddun.org/go) is the recently launched light-weight variant.*

 

  

### 1 - Understand what privacy is about

Privacy is not a synonym for confidentiality. Clearly, protecting access to data in general is an important aspect to ensure privacy, but in essence it remains a security property. Even a perfectly secure system (if that would even exist) could still violate the privacy of its users. Privacy is more concerned about what can be done with the data once someone has access to them (whether this was intentional or not) and what can be done to prevent this.

[LINDDUN](https://www.linddun.org) encapsulates and supports 7 privacy threat categories:

- **Linkability** - Two (or more) items of interest can be linked, even without knowing the identity of the data subject(s) involved.

-  **Identifiability** - A data subject can be identified from a set of data subjects through an item of interest.

- **Non-repudiation** - The data subject is unable to deny a claim (e.g. having performed an action or sent a request).

-  **Detectability** - It is possible to distinguish whether an item of interest about a data subject exists or not, regardless of being able to read the contents itself.

- **Disclosure of information** - An adversary is able to learn the content of an item of interest about a data subject. 

- **Unawareness** - The data subject is unaware of, or unable to intervene in, the collection, processing, storage, or sharing activities (and corresponding purposes) of the data subject’s personal data, and their own rights related to these data. 

- **Non-compliance** - The processing, storage, or handling of personal data is not compliant with legislation, regulation and/or policy. 

In addition to LINDDUN, you might find other privacy taxonomies useful, such as [Solove’s privacy taxonomy](https://www.law.upenn.edu/journals/lawreview/articles/volume154/issue3/Solove154U.Pa.L.Rev.477(2006).pdf), [Hansen et al.’s privacy goals](https://www.computer.org/csdl/pds/api/csdl/proceedings/download-article/17D45WXIkFp/pdf)  (i.e. intervenability, transparency, linkability), and [NIST’s privacy engineering objectives](https://nvlpubs.nist.gov/nistpubs/ir/2017/NIST.IR.8062.pdf) (i.e. predictability, manageability, disassociability).



### 2 - Get rid of your security mindset

This is probably the most challenging one for those who are familiar with (security) threat modeling. While the essence of threat modeling (i.e. think about what can go wrong in a structured way) remains the same and there is a strong dependency between privacy and security, privacy threat modeling approaches the system from a different perspective. **Rather than protecting *your* assets, privacy is about protecting the data subjects’ data and their right to privacy.** Not only (external) attackers can bring harm, also the system itself can misbehave and violate a person’s privacy. Therefore, you need to think about it with the data subject in mind and also critically reflect on the actions the system is performing on the personal data. For instance, do we need *all* these data or is a subset sufficient? What are the consequences of storing or sharing this dataset and what will (other) people be able to ‘learn’ from it?

 

### 3 - Find the approach that suits your needs

There are different ways to actually apply privacy threat modeling. Even within a single framework, method or knowledge base, execution can vary.

LINDDUN has 3 main variants to elicit privacy threats:

- **Full-fledged threat modeling** (‘*full’ [LINDDUN](https://www.linddun.org/linddun)*) - Inspired by STRIDE (as described by [Howard&Lipner](https://download.microsoft.com/download/8/1/6/816C597A-5592-4867-A0A6-A0181703CD59/Microsoft_Press_eBook_TheSecurityDevelopmentLifecycle_PDF.pdf)), LINDDUN provides systematic support to elicit and mitigate privacy threats. In summary, each system component (i.e. DFD element) needs to be examined with the LINDDUN threat categories in mind to determine whether threats apply. To help elicit these threats, LINDDUN provides privacy threat trees which describe the most common privacy threat types. *This variant is most suited for those looking for an extensive analysis with strong traceability of the process they executed.*

* **Acronym-based brainstorming** (*LINDDUN as mnemonic*) – At the other end of the spectrum is a more freestyle type of exercise. In practice, people sometimes only use the LINDDUN categories as input for a brainstorming session. While this highly reduces the effort required, it also reduces the systematicity and traceability of the process. In addition, the output solely depends on the threat modeler’s (privacy) expertise. *This variant is therefore most suited for an experienced threat modeler who is looking for a quick, rather than an exhaustive, result.*
* **Guided light-weight threat modeling** *([LINDDUN GO](https://www.linddun.org/go))* -  LINDDUN GO aims to bridge the gap between the previous two variants by combining the best of both worlds. Inspired by the [Elevation of Privilege cards](https://www.microsoft.com/en-us/download/details.aspx?id=20303), LINDDUN GO provides light-weight support by reducing the complexity of both the threat modeling process and the provided privacy knowledge while still maintaining systematicity and extensive knowledge support. *This variant is thus suited for people who are relatively new to the field, as well as for those who prefer more light-weight support in general.* 

 Overall, the less (privacy) expertise you have, the more you will need to find support in a threat modeling method and its corresponding knowledge base.  



**To conclude, remember that privacy isn’t the same as security, hence you should also approach it differently. LINDDUN provides you with different approaches, from informal to systematic, that can support you in doing so.**
