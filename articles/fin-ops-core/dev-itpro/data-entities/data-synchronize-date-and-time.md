---
title: مزامنة التاريخ والوقت في مهام الاستيراد
description: استخدم مناطق زمنيه UTC في استيراد المهام لتجنب المشكلات التي تتعلق بتحويلات المنطقة الزمنيه.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ce3bf39e8342d3fe19a253f6d17684b2bd0aec0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570469"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="cd81f-103">مزامنة التاريخ والوقت في مهام الاستيراد</span><span class="sxs-lookup"><span data-stu-id="cd81f-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd81f-104">من المهم تعيين المنطقة الزمنيه لمهمة الاستيراد الخاصة بك إلى التوقيت العالمي المتفق عليه (UTC).</span><span class="sxs-lookup"><span data-stu-id="cd81f-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="cd81f-105">قد تري تواريخ وأوقات غير متوقعه في البيانات المستوردة إذا كنت تستخدم اعدادا مختلفا.</span><span class="sxs-lookup"><span data-stu-id="cd81f-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="cd81f-106">وبدون الاعداد الصحيح، تقوم عمليه الاستيراد بتحويل تاريخ UTC إلى التنسيق المحلي، ثم تقوم إعدادات النظام بتحويله مره أخرى.</span><span class="sxs-lookup"><span data-stu-id="cd81f-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="cd81f-107">يتسبب هذا التحويل الثنائي علي التسبب في تغيير التواريخ بين التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="cd81f-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="cd81f-108">علي سبيل المثال، قد يتسبب التحويل الثنائي في ان يكون تاريخ بدء الموظف مختلفا بين Dynamics 365 Human Resources وDynamics 365 Finance بسبب الاختلافات في المناطق الزمنيه المحلية.</span><span class="sxs-lookup"><span data-stu-id="cd81f-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="cd81f-109">ويؤدي تعيين مهمة الاستيراد إلى UTC إلى حل هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="cd81f-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="cd81f-110">في Dynamics 365 Finance and Operations، حدد **أداره البيانات**.</span><span class="sxs-lookup"><span data-stu-id="cd81f-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="cd81f-111">حدد **استيراد** المشاريع، ثم حدد المشروع.</span><span class="sxs-lookup"><span data-stu-id="cd81f-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="cd81f-112">ضمن **تنسيق** التاريخ المصدر ، حدد **CSV-Unicode**.</span><span class="sxs-lookup"><span data-stu-id="cd81f-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="cd81f-113">[![تغيير تنسيق التاريخ المصدر إلى UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="cd81f-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="cd81f-114">تغيير **المنطقة الزمنيه** إلى **منطقه التوقيت العالمي المتفق عليها**، وتغيير **اللغة** إلى **En-US**.</span><span class="sxs-lookup"><span data-stu-id="cd81f-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]