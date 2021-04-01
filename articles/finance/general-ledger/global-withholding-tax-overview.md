---
title: ضريبة الخصم العمومية
description: يوفر هذا الموضوع معلومات حول وظيفة ضريبة الخصم العامة وكيفية إعدادها. يتم تحسين وظيفة ضريبة الخصم العامة لحركات المورد والعميل، بحيث يتم حساب ضريبة الخصم على مستوى الصنف.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 25fc503d6145872b8e9f28b8d9a4d7b9c1ba53a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249157"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="31c45-104">ضريبة الخصم العمومية</span><span class="sxs-lookup"><span data-stu-id="31c45-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31c45-105">يوفر هذا الموضوع معلومات حول وظيفة ضريبة الخصم العامة ويشرح كيفية إعدادها.</span><span class="sxs-lookup"><span data-stu-id="31c45-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="31c45-106">تتوفر الوظيفة الجديدة في الإصدار 10.0.17 والإصدارات اللاحقة.</span><span class="sxs-lookup"><span data-stu-id="31c45-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="31c45-107">يتم تحسين وظيفة ضريبة الخصم العامة لحركات المورد والعميل، بحيث يتم حساب ضريبة الخصم على مستوى الصنف.</span><span class="sxs-lookup"><span data-stu-id="31c45-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="31c45-108">يمكن تسوية الرصيد في حساب ضريبة الخصم من حركات الشراء من خلال تشغيل مهمة دفع ضريبة الخصم مقابل حساب تسوية ضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="31c45-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="31c45-109">لا تدعم ضريبة الخصم العامة وظيفة **الاحتفاظ بالتكاليف** في صفحات أمر الشراء وفاتورة المورد وأمر المبيعات.</span><span class="sxs-lookup"><span data-stu-id="31c45-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="31c45-110">تشغيل ضريبة الخصم العمومية</span><span class="sxs-lookup"><span data-stu-id="31c45-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="31c45-111">في مساحة عمل **إدارة الميزات**، حدد **ضريبة الخصم العمومية**، ثم حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="31c45-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="31c45-112">انتقل إلى **الضريبة \> الإعداد \> المعلمات \> معلمات دفتر الأستاذ العام**، ثم ، في علامة التبويب **ضريبة الخصم**، قم بتعيين خيار **تمكين ضريبة الخصم العامة** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="31c45-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="31c45-113">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="31c45-113">Select **Save**.</span></span>
4. <span data-ttu-id="31c45-114">قم بتحديث الصفحة في مستعرض الويب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="31c45-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="31c45-115">لا يمكن تشغيل وظيفة ضريبة الخصم العالمية للبلدان/المناطق التي توجد فيها حلول ضريبة الخصم المترجمة بالفعل.</span><span class="sxs-lookup"><span data-stu-id="31c45-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="31c45-116">وتتضمن هذه المناطق ولكن لا تقتصر على الهند والبرازيل وتايلاند والمملكة العربية السعودية والبرازيل والبريطانيا العظيمة والولايات المتحدة.</span><span class="sxs-lookup"><span data-stu-id="31c45-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]