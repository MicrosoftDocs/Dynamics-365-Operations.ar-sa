---
title: يعمل التخطيط الرئيسي على إنشاء أوامر مخططة للمنتجات الوهمية
description: يتم إنشاء الأوامر المخططة للمنتجات الوهمية بعد تشغيل التخطيط الرئيسي.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026242"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="1c7ab-103">يعمل التخطيط الرئيسي على إنشاء أوامر مخططة للمنتجات الوهمية</span><span class="sxs-lookup"><span data-stu-id="1c7ab-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="1c7ab-104">رقم KB: 4614729</span><span class="sxs-lookup"><span data-stu-id="1c7ab-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="1c7ab-105">العلامات</span><span class="sxs-lookup"><span data-stu-id="1c7ab-105">Symptoms</span></span>

<span data-ttu-id="1c7ab-106">يتم إنشاء الأوامر المخططة للمنتجات الوهمية بعد تشغيل التخطيط الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="1c7ab-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="1c7ab-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="1c7ab-107">Resolution</span></span>

<span data-ttu-id="1c7ab-108">يحدد إعداد الخيار **صنف وهمي** الخاص بالمنتجات التي تم إصدارها نوع البند الافتراضي في شجرة المواد (BOM).</span><span class="sxs-lookup"><span data-stu-id="1c7ab-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="1c7ab-109">عند تعيين الخيار **صنف وهمي** على *نعم*، سيستمر النظام في إنشاء أوامر مخططة للصنف، ولكن يتم تعيين الخيار **متطلب مشتق مباشرة** لكل أمر مخطط على *نعم*.</span><span class="sxs-lookup"><span data-stu-id="1c7ab-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="1c7ab-110">وبالتالي، لا يمكن تأكيد أمر الإنتاج المخطط بنفسه.</span><span class="sxs-lookup"><span data-stu-id="1c7ab-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="1c7ab-111">وبدلاً من ذلك، سيتم تضمينها تلقائيًا عند تأكيد أمر الإنتاج الأصلي.</span><span class="sxs-lookup"><span data-stu-id="1c7ab-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="1c7ab-112">بالإضافة إلى ذلك، سيتم تضمين بنود قائمة مكونات الصنف (BOM) للصنف الوهمي المخطط في قائمة مكونات الصنف (BOM) لأمر الإنتاج الأصلي.</span><span class="sxs-lookup"><span data-stu-id="1c7ab-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
