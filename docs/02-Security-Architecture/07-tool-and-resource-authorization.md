# Tool and Resource Authorization

Tools do not own access rights. Tools consume access rights.

## Examples

### Database tool
- allowed schemas
- allowed views
- allowed columns
- allowed query patterns
- read/write separation

### API tool
- allowed endpoints
- allowed methods
- request validation
- response filtering

### File tool
- allowed buckets
- allowed folders
- allowed objects
- data loss prevention controls

### SaaS connector
- allowed business objects
- allowed operations
- tenant scoping
- object masking

This ensures that even a correctly authenticated tool cannot overreach its authorization scope.
