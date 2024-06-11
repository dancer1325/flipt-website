- Namespaces
    - ALL resources ([Flags](https://www.notion.so/Flags-c79896bedf9743229dc2c4881a43770a?pvs=21), [Segments](https://www.notion.so/Segments-8573afbf80694b52a16550f799e1e991?pvs=21), [Rules](https://www.notion.so/Rules-bc6b9452564d473d88ecceae73af1a5d?pvs=21), ..) — belong to — 1! namespace
        - == way to organize all resources
        - →
            - ALL data / namespace — is ONLY accesible — within that namespace
        - if you do NOT select a namespace → created under ‘Default’
    - allows
        - separating ALL data /
            - environments
            - teams
            - …
    - how to configure it?
        - Flipt UI, settings
          - TODO:

- Flags
    - := basic unit in Flipt
      - **Note:** Check OpenFeature's Feature Flag
    - uses
        - on/off toggles
        - variant & rules
    - types
        - variant
            - == several options / flag
                - given some rules → return 1! variant (string) / flag
            - default type
            - JSON attachments are allowed
        - boolean
            - return boolean value / flag
            - — can be configured with — Rollout

- Segments
    - allows
        - spliting audience / predefined slices
    - global under Namespaces
    - match types
        - ALL
            - if ALL constraints match → applied
        - ANY
            - if 1 constraint match → applied
    - constraints
        - criterias to determine the segment
        - model
          ```
           {
            property,
            type,
            operator,
            value
           }
           ```
           - `type: String | Number | Boolean | DateTime | Entity`
           - `value`
               - optional

- Rules
    - allows
        - specifying Segments / variants
            - == tying Flags — variants — Segments
            - ⚠️FIRST rule / matches → applied ⚠️
            - 👁️can be re-ordered 👁️
    - uses
        - 👁️variant flags 👁️
    - distributions
        - allows
            - return different variants / segment
                - == multi-testing

- Rollout
    - := sequence of conditions /
        - if a condition is matched / request context → boolean flag is overriden
            - ⚠️FIRST rollout / matches → applied ⚠️
              - **Note:** == Rules
            - 👁️can be re-ordered 👁️
        - types
            - threshold
                - return `true` or `false` / % of entities
            - segments match
                - if an entity matches certain Segments → return `true` or `false`
    - uses
        - 👁️boolean flags 👁️
    - allows
        - changing boolean flag | request time

- Evaluation
    - TODO:
    - entity
        - := anything / — is compared against — segments & flags