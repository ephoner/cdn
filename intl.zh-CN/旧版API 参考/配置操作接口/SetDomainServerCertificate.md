# SetDomainServerCertificate {#reference_l1t_pjl_vdb .reference}

该接口用于设置某域名下证书功能是否启用及修改证书信息。

## 请求参数 {#section_bcw_rjl_vdb .section}

|参数|类型|是否必选|示例值|描述|
|Action|String|是|SetDomainServerCertificate|系统规定参数。取值：SetDomainServerCertificate|
|DomainName|String|是|www.yourdomain.com|指定证书所属加速域名，需属于https加速类型。|
|ServerCertificateStatus|String|是|on|HTTPS证书是否启用。 取值：

 -   on：启用
-   off：不启用

 默认取值：off，不启用|
|CertName|String|否|myCert1|证书名称。|
|PrivateKey|String|否|xxxxxxxx|私钥内容，不启用证书则无需输入，配置证书请输入私钥内容。|
|Region|String|否|cn-hangzhou|地区。|
|ServerCertificate|String|否|xxxxxx|安全证书内容，不启用证书则无需输入，配置证书请输入证书内容。|
|ForceSet|String|否|1|设置为1时，忽略证书名称重复的校验，覆盖原有同名证书信息|

## 返回参数 {#section_nrn_yjl_vdb .section}

|参数|类型|示例值|描述|
|RequestId|String|16A96B9A-F203-4EC5-8E43-CB92E68F4CD8|请求ID|

## 示例 {#section_g1p_gcg_vdb .section}

**请求示例**

```

http://cdn.aliyuncs.com?Action=SetDomainServerCertificate&DomainName=test.com&CertName=myCert1&ServerCertificateStatus=on&ServerCertificate=xxx&PrivateKey=yyy&公共请求参数
```

**正常返回示例**

-   JSON格式

    ```
    {
        "RequestId":"0AEDAF20-4DDF-4165-8750-47FF9C1929C9"
    }
    ```


**异常返回示例**

-   JSON格式

    ```
    {
        "Code":"InternalError",
        "HostId":"cdn.aliyuncs.com",
        "Message":"The request processing has failed due to some unknown error.",
        "RequestId":"16A96B9A-F203-4EC5-8E43-CB92E68F4CD8"
    }
    ```


