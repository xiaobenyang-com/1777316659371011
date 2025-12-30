# 菲律宾地理编码服务 Philippine Geocoding

提供菲律宾标准地理编码（PSGC）API访问的模型上下文协议（MCP）服务器，包含完整的菲律宾地理层级数据。
A model Context Protocol (MCP) server that provides access to the Philippine Standard Geocoding (PSGC) API, containing complete geographic hierarchical data of the Philippines.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| get_island_groups | List all island groups in the Philippines |
| get_island_group | Get specific island group by code |
| get_island_group_regions | Get all regions within a specific island group |
| get_island_group_provinces | Get all provinces within a specific island group |
| get_island_group_cities | Get all cities within a specific island group |
| get_island_group_municipalities | Get all municipalities within a specific island group |
| get_island_group_barangays | Get all barangays within a specific island group |
| get_regions | List all regions in the Philippines |
| get_region | Get specific region by code |
| get_region_provinces | Get all provinces within a specific region |
| get_region_districts | Get all districts within a specific region |
| get_region_cities | Get all cities within a specific region |
| get_region_municipalities | Get all municipalities within a specific region |
| get_region_cities_municipalities | Get all cities and municipalities within a specific region |
| get_region_sub_municipalities | Get all sub-municipalities within a specific region |
| get_region_barangays | Get all barangays within a specific region |
| get_provinces | List all provinces in the Philippines |
| get_province | Get specific province by code |
| get_province_cities | Get all cities within a specific province |
| get_province_municipalities | Get all municipalities within a specific province |
| get_province_cities_municipalities | Get all cities and municipalities within a specific province |
| get_province_sub_municipalities | Get all sub-municipalities within a specific province |
| get_province_barangays | Get all barangays within a specific province |
| get_cities | List all cities in the Philippines |
| get_city | Get specific city by code |
| get_city_barangays | Get all barangays within a specific city |
| get_municipalities | List all municipalities in the Philippines |
| get_municipality | Get specific municipality by code |
| get_municipality_barangays | Get all barangays within a specific municipality |
| get_barangays | List all barangays in the Philippines |
| get_barangay | Get specific barangay by code |
| get_districts | List all districts in the Philippines |
| get_district | Get specific district by code |
| get_district_cities | Get all cities within a specific district |
| get_district_municipalities | Get all municipalities within a specific district |
| get_district_cities_municipalities | Get all cities and municipalities within a specific district |
| get_district_sub_municipalities | Get all sub-municipalities within a specific district |
| get_district_barangays | Get all barangays within a specific district |
| search_by_name | Search for geographic entities by name across all levels (regions, provinces, cities, municipalities, barangays) |
| get_hierarchy | Get complete geographic hierarchy for a specific code (shows parent entities) |
| validate_code | Validate if a geographic code exists and return its type |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659371011](https://mcp.xiaobenyang.com/inspector/1777316659371011)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659371011](https://mcp.xiaobenyang.com/inspector/1777316659371011)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "菲律宾地理编码服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659371011/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "菲律宾地理编码服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659371011/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "菲律宾地理编码服务": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659371011",
          },
          "transport": "stdio"
        }
      }
}

```
