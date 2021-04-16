---
title: الوصول إلى البيانات المالية وبيانات مرجع الضريبة
description: يوفر هذا الموضوع معلومات حول الوصول إلى البيانات المرجعية المالية والضريبية.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: e704e093181ee9b8e712f33746b5434b5ea5dc4e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748607"
---
# <a name="access-to-finance-and-tax-reference-data"></a><span data-ttu-id="9046d-103">الوصول إلى البيانات المالية وبيانات مرجع الضريبة</span><span class="sxs-lookup"><span data-stu-id="9046d-103">Access to finance and tax reference data</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9046d-104">يحتاج كل عمل إلى مجموعة أساسية من البيانات المالية، مثل تقويم السنة المالية، والعملة المستخدمة لتنفيذ معاملات الشركة، والحسابات التي ترد إليها أو تخرج منها الأموال الخاصة بإدارة العمل ومعدلات الضرائب والتحويلات.</span><span class="sxs-lookup"><span data-stu-id="9046d-104">Every business works with a basic set of financial data, such as the fiscal calendar year, the currency that business is transacted in, the accounts that the money to run the business comes in to or goes out of, tax rates, and remittance.</span></span> <span data-ttu-id="9046d-105">توجد هذه البيانات في تطبيقات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9046d-105">This data resides in Finance and Operations apps.</span></span> <span data-ttu-id="9046d-106">ومع ذلك، فهي معروضة لتطبيق Dataverse بحيث تحصل التطبيقات المستندة إلى نموذج في Microsoft Dynamics 365 على مصدر واحد للبيانات المالية والضريبية..</span><span class="sxs-lookup"><span data-stu-id="9046d-106">However, it's exposed to Dataverse so that model-driven apps in Microsoft Dynamics 365 can have a single source for finance and tax data.</span></span> <span data-ttu-id="9046d-107">وبهذه الطريقة، تكون البيانات موحدة عبر النظام البيئي للأعمال.</span><span class="sxs-lookup"><span data-stu-id="9046d-107">In this way, data is uniform across the business ecosystem.</span></span> 

<span data-ttu-id="9046d-108">تتكامل البيانات المالية والضريبية باستخدام التعيينات التالية:</span><span class="sxs-lookup"><span data-stu-id="9046d-108">Finance and tax data is integrated by using the following mappings:</span></span>

+ [<span data-ttu-id="9046d-109">دفتر الأستاذ المتكامل</span><span class="sxs-lookup"><span data-stu-id="9046d-109">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="9046d-110">أصل الضريبة المتكاملة</span><span class="sxs-lookup"><span data-stu-id="9046d-110">Integrated tax master</span></span>](tax-mapping.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]