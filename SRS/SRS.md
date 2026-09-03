# 📄 Software Requirements Specification (SRS)

## 1. Inngangur
### 1.1 Tilgangur
Stutt lýsing á tilgangi kerfisins og hverju það á að skila.

### 1.2 Umfang og mörk kerfisins

Lýsið í stuttu máli hvað fellur innan marka kerfisins og hvað fellur utan þeirra.
Tilgreinið helstu samskipti kerfisins við umhverfi sitt.

### 1.3 Skilgreiningar
| Hugtak | Skýring |
|--------|---------|
| SRS | Software Requirements Specification |


### 1.4 Tilvísanir
- ISO/IEC/IEEE International Standard - Systems and software engineering -- Life cycle processes -- Requirements engineering," in ISO/IEC/IEEE 29148:2018(E) , vol., no., pp.1-104, 30 Nov. 2018, doi: 10.1109/IEEESTD.2018.8559686.ISO/IEC/IEEE 29

---

## 2. Almenn lýsing
### 2.1 Notendahópar
- Lýsa helstu notendahópum kerfisins (t.d. notendur, stjórnendur).

### 2.2 Viðskiptaávinningur
- Hver er ávinningurinn fyrir fyrirtæki eða notendur?

---

## 3. Kröfur fyrir kerfið

### 3.1 Viðskiptakröfur
| ID                                        | Titill                    |
|-------------------------------------------|---------------------------|
| [BREQ-1](business_requirements.md#breq-1) | [Titill á viðskiptakröfu] |
| [BREQ-2](business_requirements.md#breq-2) | [Titill á viðskiptakröfu] |

### 3.2 Kerfiskrafa
| ID                              | Titill                 |
|---------------------------------|------------------------|
| [SR-1](system_requirement.md#sr-1) | [Titill á kerfiskröfu] |

### 3.3 Eiginleikar (Features)
| ID                     | Titill                 |
|------------------------|------------------------|
| [F-1](feature.md#f-1)  | [Titill á eiginleika]  |
| [F-2](feature.md#f-2)  | [Titill á eiginleika]  |
| [F-3](feature.md#f-3)  | [Titill á eiginleika]  |

### 3.4 Notendakröfur
| ID                                   | Titill                  | Eiginleiki |
|--------------------------------------|-------------------------|------------|
| [UR-1](user_requirement.md#ur-1)     | [Titill á notendakröfu] | F-1        |
| [UR-2](user_requirement.md#ur-2)     | [Titill á notendakröfu] | F-1        |
| [UR-3](user_requirement.md#ur-3)     | [Titill á notendakröfu] | F-2        |
| [UR-4](user_requirement.md#ur-4)     | [Titill á notendakröfu] | F-2        |
| [UR-5](user_requirement.md#ur-5)     | [Titill á notendakröfu] | F-3        |
| [UR-6](user_requirement.md#ur-6)     | [Titill á notendakröfu] | F-3        |

### 3.5 Virknikröfur
| ID                                          | Titill                                      | Notendakrafa |
|---------------------------------------------|---------------------------------------------|--------------|
| [FR-1](functional_requirement.md#fr-1)      | [Virkni sem styður notendakröfu, titill]    | UR-1         |
| [FR-2](functional_requirement.md#fr-2)      | [Önnur virkni, titill]                      | UR-1         |
| [FR-3](functional_requirement.md#fr-3)      | [Önnur virkni, titill]                      | UR-1         |
| [FR-4](functional_requirement.md#fr-4)      | [Virkni]                                    | UR-2         |
| [FR-5](functional_requirement.md#fr-5)      | [Virkni]                                    | UR-2         |
| [FR-6](functional_requirement.md#fr-6)      | [Virkni]                                    | UR-2         |
| [FR-7](functional_requirement.md#fr-7)      | [Virkni]                                    | UR-3         |
| [FR-8](functional_requirement.md#fr-8)      | [Virkni]                                    | UR-3         |
| [FR-9](functional_requirement.md#fr-9)      | [Virkni]                                    | UR-3         |
| [FR-10](functional_requirement.md#fr-10)    | [Virkni]                                    | UR-4         |
| [FR-11](functional_requirement.md#fr-11)    | [Virkni]                                    | UR-4         |
| [FR-12](functional_requirement.md#fr-12)    | [Virkni]                                    | UR-4         |
| [FR-13](functional_requirement.md#fr-13)    | [Virkni]                                    | UR-5         |
| [FR-14](functional_requirement.md#fr-14)    | [Virkni]                                    | UR-5         |
| [FR-15](functional_requirement.md#fr-15)    | [Virkni]                                    | UR-5         |
| [FR-16](functional_requirement.md#fr-16)    | [Virkni]                                    | UR-6         |
| [FR-17](functional_requirement.md#fr-17)    | [Virkni]                                    | UR-6         |
| [FR-18](functional_requirement.md#fr-18)    | [Virkni]                                    | UR-6         |

### 3.6 Viðskiptareglur
| ID                                  | Titill                     |
|-------------------------------------|----------------------------|
| [BRG-1](business_rule.md#brg-1)     | [Viðskiptaregla, titill]   |
| [BRG-2](business_rule.md#brg-2)     | [Viðskiptaregla, titill]   |

### 3.7 Gæðaeiginleikar
| ID                                      | Titill                     |
|-----------------------------------------|----------------------------|
| [QA-1](quality_attribute.md#qa-1)       | [Gæðaeiginleiki, titill]   |
| [QA-2](quality_attribute.md#qa-2)       | [Gæðaeiginleiki, titill]   |

### 3.8 Takmarkanir
| ID                              | Titill                |
|---------------------------------|-----------------------|
| [C-1](constraint.md#c-1)        | [Takmörkun, titill]   |
| [C-2](constraint.md#c-2)        | [Takmörkun, titill]   |

### 3.9 Ytri skil (Interfaces)
| ID                                      | Titill                |
|-----------------------------------------|-----------------------|
| [UI-1](external_interface.md#ui-1)      | [Ytri skil, titill]   |
| [UI-2](external_interface.md#ui-2)      | [Ytri skil, titill]   |

---

## 4. Viðaukar
### 4.1 Orðalisti
- Skilgreina lykilhugtök.

  | Hugtak | Skilgreining |
  |--------|--------------|
  |        |              |
  |        |              |

### 4.2 Samþykktir
- Kennari: ____________________  
- Nemandi: ____________________
