---
title: مزامنة التاريخ والوقت في مهام الاستيراد
description: استخدم مناطق زمنيه UTC في استيراد المهام لتجنب المشكلات التي تتعلق بتحويلات المنطقة الزمنيه.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae04b09a68e64d6d70c0329e689ab08c3903fca0
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798709"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="c16b8-103">مزامنة التاريخ والوقت في مهام الاستيراد</span><span class="sxs-lookup"><span data-stu-id="c16b8-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c16b8-104">من المهم تعيين المنطقة الزمنيه لمهمة الاستيراد الخاصة بك إلى التوقيت العالمي المتفق عليه (UTC).</span><span class="sxs-lookup"><span data-stu-id="c16b8-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="c16b8-105">قد تري تواريخ وأوقات غير متوقعه في البيانات المستوردة إذا كنت تستخدم اعدادا مختلفا.</span><span class="sxs-lookup"><span data-stu-id="c16b8-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="c16b8-106">وبدون الاعداد الصحيح، تقوم عمليه الاستيراد بتحويل تاريخ UTC إلى التنسيق المحلي، ثم تقوم إعدادات النظام بتحويله مره أخرى.</span><span class="sxs-lookup"><span data-stu-id="c16b8-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="c16b8-107">يتسبب هذا التحويل الثنائي علي التسبب في تغيير التواريخ بين التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="c16b8-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="c16b8-108">علي سبيل المثال، قد يتسبب التحويل الثنائي في ان يكون تاريخ بدء الموظف مختلفا بين Dynamics 365 Human Resources وDynamics 365 Finance بسبب الاختلافات في المناطق الزمنيه المحلية.</span><span class="sxs-lookup"><span data-stu-id="c16b8-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="c16b8-109">ويؤدي تعيين مهمة الاستيراد إلى UTC إلى حل هذه المشكلة.</span><span class="sxs-lookup"><span data-stu-id="c16b8-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="c16b8-110">في Dynamics 365 Finance and Operations، حدد **أداره البيانات**.</span><span class="sxs-lookup"><span data-stu-id="c16b8-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="c16b8-111">حدد **استيراد** المشاريع، ثم حدد المشروع.</span><span class="sxs-lookup"><span data-stu-id="c16b8-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="c16b8-112">ضمن **تنسيق** التاريخ المصدر ، حدد **CSV-Unicode**.</span><span class="sxs-lookup"><span data-stu-id="c16b8-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="c16b8-113">[![تغيير تنسيق التاريخ المصدر إلى UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="c16b8-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="c16b8-114">تغيير **المنطقة الزمنيه** إلى **منطقه التوقيت العالمي المتفق عليها**، وتغيير **اللغة** إلى **En-US**.</span><span class="sxs-lookup"><span data-stu-id="c16b8-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>


