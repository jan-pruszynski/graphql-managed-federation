# graphql-managed-federation
GraphQL managed federation example implementation in Go

Not so obvious steps to reproduce

#### 1. Set up account at https://studio.apollographql.com

#### 2. Create new graph (deployed) and copy values for environment variables 

#### 3. Set environment variables for API Gateway service. 
```
APOLLO_KEY=EXAMPLE_KEY
APOLLO_GRAPH_ID=example-graph-name
APOLLO_GRAPH_VARIANT=current
APOLLO_SCHEMA_CONFIG_DELIVERY_ENDPOINT=https://uplink.api.apollographql.com/
```
#### 4. Create Subgraph service 

#### 5. Install rover
```
npm i -g @apollo/rover
```

#### 6. Publish your subgraph service 
```
rover subgraph publish example-graph-core@current \
		--name $SERVICE_NAME \
		--routing-url $SERVICE_URL_ADDRESS \
		--schema ./graph/schema.graphqls \ 
		--convert
